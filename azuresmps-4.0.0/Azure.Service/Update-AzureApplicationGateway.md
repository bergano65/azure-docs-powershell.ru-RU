---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075844"
---
# Update-AzureApplicationGateway

## КРАТКИй обзор
Обновляет шлюз приложения.

## Максимальное

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Update-AzureApplicationGateway** обновляет существующий шлюз приложений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение шлюза приложений с использованием его имени
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

Первая команда останавливает шлюз приложений с именем ApplicationGateway06.
Прежде чем можно будет изменить виртуальную сеть или подсеть, необходимо остановить шлюз приложения.

Вторая команда изменяет виртуальную подсеть и подсети для шлюза приложения с именем ApplicationGateway06.

### Пример 2: изменение дополнительных свойств шлюза приложения
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Эта команда изменяет количество экземпляров, размер шлюза и описание для шлюза приложения с именем ApplicationGateway06.
Эта команда не изменяет виртуальную сеть или подсети для шлюза приложения.
Таким образом, перед выполнением этой команды вам не нужно останавливать шлюз приложений.

### Пример 3: изменение шлюза приложений с помощью конвейера
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

Первая команда получает шлюз приложения с именем ApplicationGateway06 с помощью командлета **Get-AzureApplicationGateway** .
Команда сохраняет его в переменной $ApplicationGateway.

Вторая команда присваивает свойству **GatewaySize** значение Medium.

Последняя команда передает обновленный $ApplicationGateway текущему командлету.

## ПАРАМЕТРЫ

### -Описание
Указывает описание, назначаемое этим командлетом шлюзу приложений.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewaySize
Указывает размер, назначаемый этим командлетом шлюзу приложений.
Допустимые значения:

- Малого
- Канал
- Достаточ

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceCount
Указывает количество экземпляров, назначаемых этим командлетом шлюзу приложений.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя шлюза приложений, который обновляется этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -Подсети
Указывает массив подсетей, в котором этот командлет развертывает шлюз приложения.

Вы не можете обновлять подсети, пока запущен шлюз приложений.
Чтобы остановить шлюз приложения, используйте командлет Stop-AzureApplicationGateway.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
Указывает виртуальную сеть, в которой этот командлет развертывает шлюз приложения.

Вы не можете обновить виртуальную сеть, пока запущен шлюз приложений.
Чтобы остановить шлюз приложения, используйте **Stop-AzureApplicationGateway**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[New-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Остановить-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
