---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518626"
---
# Get-AzIotHubConfiguration

## SYNOPSIS
Здесь перечислены все или конкретная конфигурация автоматического управления устройствами в режиме IoT.

## СИНТАКСИС

### Набор ресурсов (по умолчанию)
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObjectSet
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdSet
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Сведения о настройке автоматического управления устройствами в режиме IoT или списке конфигураций автоматического управления устройствами в центре IoT.
Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management сведения см. в этой области.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

Получите сведения о настройке автоматического управления устройствами в режиме IoT.

### Пример 2
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

Автоматические настройки управления устройствами со списком IoT в центре IoT.

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

### -InputObject
Объект IotHub

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IotHubName
Имя концентратора Iot

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Идентификатор конфигурации.

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

### -ResourceGroupName
Имя группы ресурсов

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ИД ресурса IotHub

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration

### Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
