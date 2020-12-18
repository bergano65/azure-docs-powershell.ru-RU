---
title: Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell
description: Узнайте, как выполнить автоматическую миграцию скриптов PowerShell из AzureRM в модуль Az PowerShell
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488536"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell

В этой статье показано, как использовать модуль Az.Tools.Migration PowerShell для автоматической миграции скриптов PowerShell и модулей скриптов из AzureRM в модуль Az PowerShell.

> [!IMPORTANT]
> Модуль PowerShell Az.Tools.Migration сейчас предоставляется в общедоступной предварительной версии. Эта предварительная версия предоставляется без соглашения об уровне обслуживания. Эта версия не рекомендуется для использования с рабочими нагрузками в производственной среде. Некоторые функции могут не поддерживаться или их возможности могут быть ограничены. Дополнительные сведения см. в статье [Дополнительные условия использования предварительных выпусков Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

## <a name="requirements"></a>Требования

* Обновите существующие скрипты PowerShell до последней версии [модуля AzureRM PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Установите модуль Az.Tools.Migration PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Шаг 1. Создание плана обновления

Используйте командлет **`New-AzUpgradeModulePlan`** , чтобы создать план обновления для переноса скриптов и модулей в модуль Az PowerShell. Этот командлет не вносит никаких изменений в существующие скрипты. Используйте параметр **`FilePath`** для определенного скрипта или параметр **`DirectoryPath`** для выбора всех скриптов в определенной папке.

> [!NOTE]
> Командлет **`New-AzUpgradeModulePlan`** не выполняет план, а только создает только шаги по обновлению.

В следующем примере создается план для всех скриптов в папке _`C:\Scripts`_ . Параметр **`OutVariable`** указан, поэтому результаты возвращаются и сохраняются в переменной с именем **`Plan`** .

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Как показано в следующих выходных данных, в этом плане обновления указан определенный файл и точки смещения, которые нужно изменить при переходе от AzureRM к командлетам Az PowerShell.

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

Перед выполнением обновления необходимо просмотреть результаты плана для проблем. В следующем примере возвращается список скриптов и элементов в этих скриптах, которые не позволяют автоматически обновлять их.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

Элементы, показанные в следующих выходных данных, не будут обновляться автоматически без предварительного устранения проблем. Известные проблемы, которые препятствуют автоматическому обновлению, связаны с командами, использующими сплаттинг.

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a>Шаг 2. Выполнение обновления

> [!CAUTION]
> Операция отмены не предусмотрена. Обязательно убедитесь, что существует резервная копия скриптов и модулей PowerShell, которые вы пытаетесь обновить.

Когда вас будет устраивать план, обновление будет выполнено с помощью командлета **`Invoke-AzUpgradeModulePlan`** . Укажите **`SaveChangesToNewFiles`** для значения параметра **`FileEditMode`** , чтобы предотвратить внесение изменений в исходные скрипты. При использовании этого режима обновление выполняется путем создания копии каждого скрипта, используемого с _`_az_upgraded`_ при добавлении к именам файлов.

> [!WARNING]
> Действие командлета **`Invoke-AzUpgradeModulePlan`** может оказаться разрушительным, если указан параметр **`-FileEditMode ModifyExistingFiles`** ! Это приведет к непосредственному изменению скриптов и функций в соответствии с планом обновления модуля, созданным командлетом **`New-AzUpgradeModulePlan`** . Чтобы сохранить возможность восстановить прежнее состояние, укажите параметр **`-FileEditMode SaveChangesToNewFiles`** .

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

Если в результатах будут ошибки, их можно изучить с помощью следующей команды:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a>Ограничения

* Автоматическое обновление имени параметра в формат параметров с символом @ не поддерживается. Если такие параметры будут обнаружены во время создания плана обновления, отобразится предупреждение.
* Операции файлового ввода-вывода используют кодировку по умолчанию. Нетипичные сценарии использования кодировки файлов могут вызвать проблемы.
* Командлеты AzureRM, переданные в качестве аргументов в инструкции макетирования модульного тестирования Pester, не обнаруживаются.
* Сейчас в качестве целевого объекта поддерживается только модуль Az PowerShell версии 4.6.1.

## <a name="how-to-report-issues"></a>Отправка сообщений о проблемах

Вы можете оставить свой отзыв и сообщить о проблемах, связанных с модулем Az.Tools.Migration PowerShell, в разделе [проблем GitHub](https://github.com/Azure/azure-powershell-migration/issues) в репозитории `azure-powershell-migration`.

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения о модуле Az PowerShell см. в [документации по Azure PowerShell](/powershell/azure/).