---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518505"
---
# Get-AzIotCentralApp

## SYNOPSIS
Свойства одного или нескольких центрального приложения IoT.

## СИНТАКСИС

### ListIotCentralAppsParameterSet (по умолчанию)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Возвращает метаданные для определенного центрального приложения IoT или всех приложений в группе ресурсов или подписке в зависимости от набора параметров. 

## ПРИМЕРЫ

### Пример 1. Получение определенного центрального приложения IoT.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Возвращает метаданные для указанного центрального приложения IoT.

Пример выходных данных:

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName

### Пример 2. Получение центрального приложения IoT в подписке.
```powershell
PS C:\> Get-AzIotCentralApp
```

Возвращает метаданные для всех центральных приложений IoT в текущей подписке.

Пример выходных данных:

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX DisplayName: My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName2

### Пример 3. Получение центрального приложения IoT в группе ресурсов.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Возвращает метаданные для всех центрального приложения IoT в предоставленной группе ресурсов.

Пример выходных данных:

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX DisplayName : My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName

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

### -Name
Имя центрального ресурса приложения IOT.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Iot Central Application Resource Id.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
