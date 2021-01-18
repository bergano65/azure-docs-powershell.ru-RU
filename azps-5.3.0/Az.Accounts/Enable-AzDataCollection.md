---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516826"
---
# Enable-AzDataCollection

## SYNOPSIS
Позволяет Azure PowerShell собирать данные для улучшения пользовательского интерфейса с помощью cmdlets Azure PowerShell. При выполнении этого cmdlet выполняется сбор данных текущего пользователя на текущем компьютере. Данные собираются по умолчанию, если вы явным образом не откажетлись от них.

## СИНТАКСИС

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ

Этот `Enable-AzDataCollection` cmdlet используется для использования сбора данных. Azure PowerShell по умолчанию автоматически собирает данные телеметрии. Корпорация Майкрософт собирает собранные данные для выявления шаблонов использования, выявления распространенных проблем и улучшения работы Azure PowerShell.
Microsoft Azure PowerShell не собирает личные или личные данные. Чтобы отключить сбор данных, необходимо явно отказаться от нее путем выполнения `Disable-AzDataCollection` .

## ПРИМЕРЫ

### Пример 1. Включение сбора данных для текущего пользователя

В следующем примере показано, как включить сбор данных для текущего пользователя.

```powershell
Enable-AzDataCollection
```

## PARAMETERS

### -DefaultProfile

Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Confirm

Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)

## INPUTS

### Нет

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
