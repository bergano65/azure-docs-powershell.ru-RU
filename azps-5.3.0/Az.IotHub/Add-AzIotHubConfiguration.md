---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: d84d5b172d1a22880b508f8b43f071d5d454cf38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518654"
---
# Add-AzIotHubConfiguration

## SYNOPSIS
Добавление конфигурации автоматического управления устройствами из IoT в целевой центр IoT.

## СИНТАКСИС

### Набор ресурсов (по умолчанию)
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectSet
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdSet
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Содержимое конфигурации является json, и немного различается в зависимости от цели устройства или модуля. Конфигурации устройств имеют форму {"deviceContent":{...}}
Конфигурации модулей имеют форму {"moduleContent":{...}}
Конфигурации можно определить с учетом предоставленных пользователем метрик для оценки по запросу.
Метриками пользователей являются json и в виде {"queries":{...}} или {"метрики":{"запросы":{...}}}.

Примечание. Целевое условие для модулей должно начинаться с "from devices.modules where". Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management сведения см. в этой области.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

Создайте конфигурацию устройства с метаданными по умолчанию.

### Пример 2
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

Создайте конфигурацию устройства с приоритетом 3, который применяется на условии, если устройство помечено в здании 9 и среда является тестовой.

### Пример 3
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

Создайте конфигурацию устройства с метриками пользователей.

### Пример 4
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

Создайте конфигурацию устройства с метами.

### Пример 5
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

Создайте конфигурацию устройства с содержимым.

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

### -DeviceContent
Конфигурация устройств IotHub.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

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

### -Label
Карта меток, которые будут применены к конечной конфигурации.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Метрическая
Набор запросов для определения метрик конфигурации.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Вес конфигурации устройства в случае соревнований правил (самые высокие победы).

```yaml
Type: System.Int32
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

### -TargetCondition
Целевое условие, к которому применяется конфигурация устройства.

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

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
