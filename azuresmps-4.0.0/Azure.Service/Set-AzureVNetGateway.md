---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076414"
---
# Set-AzureVNetGateway

## КРАТКИй обзор
Включение или отключение VPN-шлюза для виртуальной сети Azure.

## Максимальное

### Connect (по умолчанию)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Соединения
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureVNetGateway** включает или отключает шлюз виртуальной частной сети (VPN) для виртуальной сети Azure.
Шлюз виртуальной сети — это конечная точка VPN для подключения к виртуальной сети.
Укажите параметр *подключения* или *отключения* , чтобы включить или отключить VPN-подключение между локальным сайтом локальной сети и виртуальной сетью.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Включение шлюза виртуальной сети для виртуальной сети
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Эта команда включает шлюз виртуальной сети между виртуальной сетью Azure с именем ContosoProdNet и VPN-устройством для сайта локальной сети с именем ContosoBranchOffice.

### Пример 2: Отключение шлюза виртуальной сети для виртуальной сети
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Эта команда отключает шлюз виртуальной сети между виртуальной сетью Azure с именем ContosoProdNet и VPN-устройством для сайта локальной сети с именем ContosoBranchOffice.

## ПАРАМЕТРЫ

### -Connect
Указывает на то, что этот командлет разрешает VPN-подключение между виртуальной сетью и сайтом локальной сети.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отключение
Указывает, что этот командлет отключает VPN-подключение между виртуальной сетью и сайтом локальной сети.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Задает имя локального сайта локальной сети, для которого этот командлет включит или отключит VPN-подключение.

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

### -VNetName
Указывает виртуальную сеть, для которой этот командлет включит или отключит VPN-подключение.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[New-AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Сброс — AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Изменить размер — AzureVNetGateway](./Resize-AzureVNetGateway.md)


