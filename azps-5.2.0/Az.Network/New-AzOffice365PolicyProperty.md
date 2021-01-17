---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329380"
---
# New-AzOffice365PolicyProperty

## SYNOPSIS
Определите новую политику разбора трафика Office 365, которая будет использоваться с сайтом виртуального устройства.

## СИНТАКСИС

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Команда New-AzOffice365PolicyProperties определяет политику разбора в Office 365, которая будет использоваться с сайтом виртуального устройства. 

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

Создайте объект политики разбора трафика Office 365, который будет использоваться с командами сайта виртуальных устройств.

## PARAMETERS

### -Allow
Разорвать трафик категории "Разрешить".

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

### -По умолчанию
Разорвать трафик категории по умолчанию.

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

### -Optimize
Разорвать трафик оптимизации категории.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
