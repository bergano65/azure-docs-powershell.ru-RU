---
title: Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell
description: Узнайте, как выполнить автоматическую миграцию скриптов PowerShell из AzureRM в модуль Az PowerShell
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856661"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell

В этой статье показано, как использовать модуль Az.Tools.Migration PowerShell для автоматической миграции скриптов PowerShell и модулей скриптов из AzureRM в модуль Az PowerShell.

> [!IMPORTANT]
> Модуль PowerShell Az.Tools.Migration сейчас предоставляется в общедоступной предварительной версии. Эта предварительная версия предоставляется без соглашения об уровне обслуживания. Эта версия не рекомендуется для использования с рабочими нагрузками в производственной среде. Некоторые функции могут не поддерживаться или их возможности могут быть ограничены. Дополнительные сведения см. в статье [Дополнительные условия использования предварительных выпусков Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Вы можете оставить свой отзыв и сообщить о проблемах, связанных с модулем Az.Tools.Migration PowerShell, в разделе [проблем GitHub](https://github.com/Azure/azure-powershell-migration/issues) в репозитории `azure-powershell-migration`.

## <a name="requirements"></a>Требования

* Обновите существующие скрипты PowerShell до последней версии [модуля AzureRM PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Установите модуль Az.Tools.Migration PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Шаг 1. Создание плана обновления

Используйте командлет `New-AzUpgradeModulePlan`, чтобы создать план обновления для переноса скриптов и модулей в модуль Az PowerShell. В этом плане обновления указан конкретный файл и точки смещения, которые нужно изменить при переходе от AzureRM к командлетам Az PowerShell.

> [!NOTE]
> Командлет `New-AzUpgradeModulePlan` не выполняет план, а только создает только шаги по обновлению.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Проверьте результаты плана обновления.

```powershell
# Show the entire upgrade plan
$Plan
```

Выполните следующую команду, чтобы отфильтровать результаты по командам с предупреждениями или ошибками. Это может быть удобным в больших результирующих наборах для быстрого поиска ошибок перед выполнением обновления.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>Шаг 2. Выполнение обновления

План обновления выполняется при запуске командлета `Invoke-AzUpgradeModulePlan`. Эта команда выполняет обновление указанных файлов или папок, кроме всех файлов и папок с ошибками, обнаруженными командлетом `New-AzUpgradeModulePlan`.

Для этой команды нужно указать, следует ли изменять файлы на месте или сохранять новые файлы вместе с исходными файлами (сохраняя исходные файлы без изменений).

> [!CAUTION]
> Операция отмены не предусмотрена. Обязательно убедитесь, что существует резервная копия скриптов и модулей PowerShell, которые вы пытаетесь обновить.

> [!WARNING]
> Действие командлета `Invoke-AzUpgradeModulePlan` может оказаться разрушительным, если указан параметр `-FileEditMode ModifyExistingFiles`! Это приведет к изменению скриптов и функций "на месте" в соответствии с планом обновления модуля, созданным командлетом `New-AzUpgradeModulePlan`. Чтобы сохранить возможность восстановить прежнее состояние, укажите параметр `-FileEditMode SaveChangesToNewFiles`.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Проверьте результаты операции обновления.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Если в результатах будут ошибки, их можно изучить с помощью следующей команды:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Ограничения

* Автоматическое обновление имени параметра в формат параметров с символом @ не поддерживается. Если такие параметры будут обнаружены во время создания плана обновления, отобразится предупреждение.
* Операции файлового ввода-вывода используют кодировку по умолчанию. Нетипичные сценарии использования кодировки файлов могут вызвать проблемы.
* Командлеты AzureRM, переданные в качестве аргументов в инструкции макетирования модульного тестирования Pester, не обнаруживаются.
* Сейчас в качестве целевого объекта поддерживается только модуль Az PowerShell версии 4.6.1.

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения о модуле Az PowerShell см. в [документации по Azure PowerShell](/powershell/azure/).