---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392924"
---
# Get-AzConnectedMachineExtension

## SYNOPSIS
Операция получения расширения.

## СИНТАКСИС

### Список (по умолчанию)
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
Операция получения расширения.

## ПРИМЕРЫ

### Пример 1. Список всех расширений для компьютера
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

Список всех расширений для определенного компьютера.

### Пример 2. Получить определенное расширение на компьютере
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

Получает определенное расширение на компьютере.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Развернуть
Выражение для расширения, применяемая к операции.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineName
Имя компьютера, содержащего расширение.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя расширения компьютера.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Учетные данные подписки, однозначно определяют подписку Microsoft Azure.
Он является частью URI каждого звонка службы.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension

## ПРИМЕЧАНИЯ

ALIASES

## СВЯЗАННЫЕ ССЫЛКИ

