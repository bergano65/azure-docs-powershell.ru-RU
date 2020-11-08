---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076429"
---
# Set-AzureApplicationGatewayConfig

## КРАТКИй обзор
Настройка шлюза приложений.

## Максимальное

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureApplicationGatewayConfig** настраивает шлюз приложения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка шлюза приложений с помощью объекта конфигурации
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

Первая команда получает объект конфигурации для шлюза приложения с именем ApplicationGateway02 с помощью командлета **Get-AzureApplicationGatewayConfig** .
Команда сохраняет его в переменной $ConfigReturnObject.

Вторая команда задает конфигурацию для приложения с именем ApplicationGateway06, используя объект конфигурации шлюза приложения, хранящийся в переменной $ConfigReturnObject.

### Пример 2: Настройка шлюза приложений с помощью файла конфигурации
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Эта команда задает конфигурацию для приложения с именем ApplicationGateway06 с помощью файла конфигурации шлюза приложений в указанном расположении.

### Пример 3: изменение конфигурации с помощью объекта конфигурации
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

Первая команда получает объект конфигурации для шлюза приложения с именем ApplicationGateway06 с помощью командлета **Get-AzureApplicationGatewayConfig** .
Команда сохраняет его в переменной $ConfigReturnObject.

Вторая команда назначает значение порта свойству **Port** в объекте, хранящемся в $ConfigReturnObject.

Последняя команда передает обновленный $ConfigReturnObject текущему командлету.

## ПАРАМЕТРЫ

### -Config
Указывает объект конфигурации шлюза приложений.
Этот командлет назначает конфигурацию, которую этот параметр указывает на шлюз приложения.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigFile
Задает путь к файлу конфигурации в формате XML для шлюза приложения.
Этот командлет назначает конфигурацию, которую этот параметр указывает на шлюз приложения.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя шлюза приложений, который настраивает этот командлет.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


