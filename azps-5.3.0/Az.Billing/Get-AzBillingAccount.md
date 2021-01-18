---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519783"
---
# Get-AzBillingAccount

## SYNOPSIS
Получить учетные записи вы выставления счетов.

## СИНТАКСИС

### Список (по умолчанию)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Один
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для получения учетных записей вычетов и доступа к ним у пользователя есть учетные записи **Get-AzBillingAccount.** 

## ПРИМЕРЫ

### Пример 1
```
PS C:\> Get-AzBillingAccount
```

Получить доступ ко всем учетным записям вы выставления счетов.

### Пример 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Получите учетную запись вы счета с указанным именем.

### Пример 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Получить доступ ко всем учетным записям вы выставления счетов и включить адрес в результат.

### Пример 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Получите доступ ко всем учетным записям вы выставления счетов и включим в результат профили вы выставления счетов.

### Пример 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Получите все учетные записи выставления счетов, к которые у пользователя есть доступ, и включит в результат профили выставления счетов и разделы счетов.

### Пример 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Получите учетную запись выставления счетов с указанным именем, включив в результат адрес, профили выставления счетов и разделы счетов.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAddress
Включив адрес учетной записи вы выставления счетов.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandBillingProfile
Включив профили вы выставления счетов в учетную запись вы выставления счетов.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandInvoiceSection
Включив в них профили выставления счетов в разделах учетной записи выставления счетов и счетах.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя определенной учетной записи вы выставления счетов.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListEntitiesToCreateSubscription
Перечислить объекты вы счета в учетной записи вы выставления счетов, которую можно использовать для создания подписки.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
