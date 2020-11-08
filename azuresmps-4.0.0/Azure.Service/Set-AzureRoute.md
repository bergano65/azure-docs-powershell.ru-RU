---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075823"
---
# Set-AzureRoute

## КРАТКИй обзор
Создает маршрут в таблице маршрутов.

## Максимальное

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRoute** создает маршрут в таблице маршрутов.
Новый маршрут вступает в силу практически сразу на виртуальных машинах, связанных с таблицей маршрутов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление виртуального устройства, маршрут следующего прыжка
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

Эта команда создает таблицу маршрутов с именем ApplianceRouteTable в указанном расположении.
Команда передает эту таблицу маршрутов в текущий командлет.
Текущий командлет добавляет маршрут с именем ApplianceRoute03, который является типом VirtualAppliance следующего прыжка.
Команда задает IP-адрес следующего прыжка и префикс адреса для маршрута.

### Пример 2: Добавление маршрутизатора следующего прыжка к Интернету
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Эта команда получает таблицу маршрутов с именем ApplianceRouteTable.
Команда передает эту таблицу маршрутов в текущий командлет.
Текущий командлет добавляет маршрут с именем InternetRoute, который является типом следующего прыжка в Интернете.
Команда задает префикс адреса для маршрута.

## ПАРАМЕТРЫ

### -AddressPrefix
Указывает префикс адреса для нового маршрута.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopIpAddress
Указывает IP-адрес устройства, которое является следующим прыжком для трафика, использующего этот маршрут.
Укажите это значение только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.

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

### -NextHopType
Указывает тип следующего прыжка для трафика, использующего этот маршрут.
Допустимые значения: 

- VPNGateway
- VNETLocal
- IIS
- VirtualAppliance
- Значения

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет. Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -RouteName
Задает имя для нового маршрута, который добавляется этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RouteTable
Указывает таблицу маршрутов, к которой этот командлет добавляет новый маршрут.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Remove-AzureRoute](./Remove-AzureRoute.md)


