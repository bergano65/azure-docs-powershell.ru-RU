---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517562"
---
# New-AzSentinelDataConnector

## SYNOPSIS
Создание соединитела данных.

## СИНТАКСИС

### AzureActiveDirectory (по умолчанию)
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AzureAdvancedThreatProtection
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureSecurityCenter
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AmazonWebServicesCloudTrail
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MicrosoftCloudAppSecurity
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MicrosoftDefenderAdvancedThreatProtection
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Office 365
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ThreatIntelligence
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания правила оповещения **New-AzSentinelAlertRule** в указанной рабочей области создается правило аналитики.
Чтобы создать правило оповещения, необходимо указать один из параметров, например -AzureActiveDirectory.  У каждого типа есть разные параметры.
Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.
Примечание. Не все соединители данных, доступные на портале, являются доступны через API.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

В этом примере создается **dataConnector** для Центра безопасности Azure в указанной рабочей области, а затем $DataConnector переменной.

### Пример 2
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

В этом примере создается **dataConnector** для Microsoft Cloud App Security в указанной рабочей области, а затем $DataConnector переменной.

## PARAMETERS

### -Оповещения
Оповещения соединитела данных

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AmazonWebServicesCloudTrail
Data Connector Amazon Web Services Cloud Trail

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AwsRoleArn
Роль AWS соединитела данных AWS Arn

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureActiveDirectory
Data Connector Azure Active Directory

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureAdvancedThreatProtection
Data Connector Azure Advanced Threat Protection

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureSecurityCenter
Data Connector Azure Security Center

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataConnectorId
Data Connector Azure Active Directory

```yaml
Type: System.String
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

### -DiscoveryLogs
Журналы обнаружения соединители данных

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exchange
Data Connector Exchange

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Индикаторы
Индикаторы соединители данных

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Logs
Журналы соединители данных

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftCloudAppSecurity
Data Connector Microsoft Cloud App Security

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftDefenderAdvancedThreatProtection
Data Connector Microsoft Defender Advanced Threat Protection

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Office365
Data Connector Office 365

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Data Connector Azure Active Directory

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

### -SharePoint
Data Connector SharePoint

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Data connector Subscription Id

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatIntelligence
Data Connector Threat Intelligence

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Data Connector Azure Active Directory

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

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет
## OUTPUTS

### Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
