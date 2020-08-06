---
title: Запуск командлетов Azure PowerShell в заданиях PowerShell
description: Сведения о параллельном запуске командлетов Azure PowerShell или запуске в качестве фоновых задач, используя -AsJob и Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 36fcfc42fed91c5a0c8eff200c662e1e31cacfb9
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566588"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Запуск командлетов Azure PowerShell в заданиях PowerShell

Azure PowerShell зависит от подключения к облаку Azure и ожидания ответов, поэтому большинство этих командлетов блокируют сеанс PowerShell до получения ответа из облака.
Задания Powershell позволяют запускать командлеты в фоновом режиме или одновременно выполнять несколько задач в Azure из одного сеанса PowerShell.

В этой статье приводится краткий обзор запуска командлетов Azure PowerShell в качестве заданий PowerShell, а также проверки их выполнения. Для запуска команд в Azure PowerShell необходимо использовать контексты Azure PowerShell, которые подробно описаны в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).
Дополнительные сведения о заданиях PowerShell, см. раздел [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Сведения о заданиях PowerShell).

## <a name="azure-contexts-with-powershell-jobs"></a>Контексты Azure с заданиями PowerShell

Задания PowerShell выполняются как отдельные процессы без подключенного сеанса PowerShell, поэтому им необходимо предоставить ваши учетные данные Azure. Учетные данные передаются как объекты контекста Azure одним из следующих способов:

* Автоматическое сохранение контекста. Сохраняемость контекста включена по умолчанию и сохраняет данные для входа в нескольких сеансах. При включенной сохраняемости контекста текущий контекст Azure передается новому процессу:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Используйте параметр `-AzContext` с любыми командлетами Azure PowerShell, чтобы предоставить объект контекста Azure:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Если сохраняемость контекста отключена, аргумент `-AzContext` является обязательным.

* Используйте переключатель `-AsJob`, предоставляемый некоторыми командлетами Azure PowerShell. Этот переключатель автоматически запускает командлет как задание PowerShell, используя текущий активный контекст Azure:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Чтобы узнать, поддерживает ли командлет `-AsJob`, проверьте его справочную документацию. Переключатель `-AsJob` не требует включения автосохранения контекста.

Состояние запущенного задания можно проверить с помощью командлета [Get-Job](/powershell/module/microsoft.powershell.core/get-job). Чтобы получить выходные данные задания, используйте командлет [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Чтобы удаленно проверять ход выполнения операции в Azure, используйте командлеты `Get-`, связанные с типом ресурса, изменяемого заданием:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>См. также:

* [Контексты Azure PowerShell](context-persistence.md)
* [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Сведения о заданиях PowerShell)
* [Справочные материалы по Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Справочные материалы по Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
