---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 65825e1cbb5da41d1557d30b0f152ee456e6e86b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566579"
---
# Set-AzureRmApplicationGatewayProbeConfig

## КРАТКИй обзор
Настройка конфигурации проверки работоспособности на существующем шлюзе приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Set-AzureRmApplicationGatewayProbeConfig задает конфигурацию проверки работоспособности на существующем шлюзе приложения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка конфигурации для проверки работоспособности на шлюзе приложений
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

Эта команда задает конфигурацию для проверки работоспособности с именем Probe05 для шлюза приложения с именем Gateway.
Кроме того, команда устанавливает для порога неработоспособности 8 повторных попыток и время ожидания после 120 секунд.

## ПАРАМЕТРЫ

### -ApplicationGateway
Указывает шлюз приложения, которому этот командлет отправляет зонд.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName
Указывает имя хоста, на которое этот командлет отправляет зонд.

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

### -Interval (интервал)
Задает интервал проверки в секундах.
Это интервал времени между двумя последовательными зондами.
Это значение находится в диапазоне от 1 секунды до 86400 секунд.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Match
Текст, который должен содержаться в ответе работоспособности.
Пустое значение по умолчанию

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
Минимальное количество серверов, которые всегда помечаются как работоспособные.
Значение по умолчанию: 0

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя зонда.

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

### -Path
Указывает относительный путь к зонду.
Допустимый путь начинается с символа косой черты (/).
Пробный зонд отправляется в \<Protocol\> :// \<host\> : \<port\> \<path\> .

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

### -PickHostNameFromBackendHttpSettings
Следует ли выбирать заголовок узла из параметров внутреннего HTTP-сервера.
Значение по умолчанию: ложь

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

### -Protocol (протокол)
Указывает протокол, используемый для отправки пробной проверки.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
Задает время ожидания пробы в секундах.
Этот командлет помечает пробу как сбой, если допустимый ответ не получен за этот период ожидания.
Допустимые значения: от 1 секунды до 86400 секунд.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyThreshold
Указывает число повторных попыток проверки.
Внутренний сервер помечается вниз после появления счетчика неудачных последовательностей проверки появления нерабочего порогового значения.
Допустимые значения находятся в диапазоне от 1 секунды до 20 секунд.

```yaml
Type: Int32
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

### PSApplicationGateway
Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmApplicationGatewayProbeConfig]()

[Get-AzureRmApplicationGatewayProbeConfig]()

[New-AzureRmApplicationGatewayProbeConfig]()

[Remove-AzureRmApplicationGatewayProbeConfig]()

