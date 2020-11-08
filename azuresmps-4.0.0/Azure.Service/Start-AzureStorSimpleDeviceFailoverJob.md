---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075776"
---
# Start-AzureStorSimpleDeviceFailoverJob

## КРАТКИй обзор
Инициирует операцию отработки отказа для групп контейнера тома.

## Максимальное

### Пустой (по умолчанию)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Start-AzureStorSimpleDeviceFailoverJob** инициирует операцию отработки отказа для одной или нескольких групп контейнера тома от одного устройства к другому.

## ИЛЛЮСТРИРУЮТ

### Пример 1: запуск задания отработки отказа для именованного устройства и именованного целевого устройства
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Эта команда получает контейнеры отказоустойчивого тома для устройства с именем ChewD_App7 с помощью командлета **Get-AzureStorSimpleFailoverVolumeContainers** .
Команда передает результаты в командлет **Where-Object** , в результате чего удаляются контейнеры со значением, отличным от $true для свойства **IsDCGroupEligibleForDR** .
Для получения дополнительных сведений введите `Get-Help Where-Object` .
Текущий командлет запускает задания отработки отказа для оставшихся контейнеров отказоустойчивого тома.
Команда задает имя устройства и имя оконечного устройства.
Команда возвращает идентификатор экземпляра задания, с которого начинается командлет.

### Пример 2: начало задания отработки отказа для устройства и оконечного устройства, указанного ИДЕНТИФИКАТОРом
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Эта команда получает контейнеры отказоустойчивого тома для устройства с именем ChewD_App7 с помощью **Get-AzureStorSimpleFailoverVolumeContainers**.
Команда передает результаты в **Where-Object** , которая удаляет эти containters со значением, отличным от $true для свойства **IsDCGroupEligibleForDR** .
Командлет передает результаты командлету **Select-Object** , выбирающему первый объект, передаваемый в текущий командлет.
Для получения дополнительных сведений введите `Get-Help Select-Object` .
Текущий командлет запускает задания отработки отказа для выбранного контейнера отказоустойчивого тома.
Команда задает идентификатор устройства и идентификатор целевого устройства.
Команда возвращает идентификатор экземпляра задания, с которого начинается командлет.

## ПАРАМЕТРЫ

### -DeviceId
Указывает ИД экземпляра устройства StorSimple, на котором находятся группы контейнеров тома.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Имя_устройства
Указывает имя устройства StorSimple, на котором находятся группы контейнеров тома.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceId
Указывает идентификатор экземпляра устройства StorSimple, которому этот командлет не проходит группы контейнера тома.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
Указывает имя устройства StorSimple, для которого этот командлет не проходит группы контейнера тома.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
Указывает список групп контейнеров томов, на которые не передается этот командлет на другое устройство.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Список\<DataContainerGroup\>
Вы можете передать в этот командлет список групп контейнера тома.

## НАПРЯЖЕНИЕ

### Подстрок

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


