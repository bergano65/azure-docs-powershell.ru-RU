---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517513"
---
# Update-AzSentinelDataConnector

## SYNOPSIS
Обновление соединитела данных.

## СИНТАКСИС

### DataConnectorId (по умолчанию)
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
В этой рабочей области **соединитель Update-AzSentinelDataConnector** обновляет соединитель данных.
Объект **DataConnector** можно передать в качестве параметра или с помощью оператора конвейера. Кроме того, можно указать необходимые параметры.
С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

Команда получает соединители данных по *DataConnectorId* и устанавливает состояние оповещений *"Отключено".*   Все остальные свойства остаются одинаковыми.

## PARAMETERS

### -Оповещения
Оповещения соединитела данных

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AwsRoleArn
Роль AWS соединитела данных AWS Arn

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataConnectorId
Data Connector Id.

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiscoveryLogs
Журналы обнаружения соединители данных

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exchange
Data Connector Exchange

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Индикаторы
Индикаторы соединители данных

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
InputObject.

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Logs
Журналы соединители данных

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ИД ресурса.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SharePoint
Data Connector SharePoint

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Data connector Subscription Id

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Имя рабочей области.

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
