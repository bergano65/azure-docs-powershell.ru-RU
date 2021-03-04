---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: c97567c2832d82ec739b62bfe8bb6c08e173f9e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012408"
---
# Get-AzConnectedMachine

## SYNOPSIS
Извлекает сведения о представлении модели или экземпляре гибридной машины.

## СИНТАКСИС

### Список1 (по умолчанию)
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Список
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Извлекает сведения о представлении модели или экземпляре гибридной машины.

## ПРИМЕРЫ

### Пример 1. Список всех подключенных компьютеров в подписке
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

Список всех подключенных компьютеров в подписке.
Если подписка не указана, она будет использовать ее из контекста Azure PowerShell.

### Пример 2. Список всех подключенных компьютеров в группе ресурсов
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

Перечислить все подключенные компьютеры в группе ресурсов.

### Пример 3. Подключение компьютера к группе ресурсов по имени
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

Получить подключенный компьютер в группе ресурсов по имени.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя гибридной машины.

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
Parameter Sets: Get, List
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

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelse

## ПРИМЕЧАНИЯ

ALIASES

## СВЯЗАННЫЕ ССЫЛКИ

