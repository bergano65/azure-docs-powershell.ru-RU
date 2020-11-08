---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065488"
---
# New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject

## КРАТКИй обзор
Создание конфигурации протокола, используемой для оценки тестов по протоколу TCP, HTTP или ICMP.

## Максимальное

### Номера
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ЧЕРЕЗ
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### -
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject создает конфигурацию протокола, используемую для оценки тестов по протоколу TCP, HTTP или ICMP.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

Порт: 80 DisableTraceRoute: ложь

## ПАРАМЕТРЫ

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

### -DisableTraceRoute
Значение, указывающее, следует ли отключить оценку пути с помощью маршрута трассировки.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpProtocol
Коммутатор протокола HTTP

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IcmpProtocol
Переключатель протокола ICMP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
Используемый HTTP-метод.

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Компонент пути универсального кода ресурса (URI). Например, \" /Dir1/Dir2 \" .

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port (порт)
Порт, к которому нужно подключиться.

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferHTTPS
Значение, указывающее, является ли протокол HTTPS предпочтительнее HTTP в случае, если выбор не является явным.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestHeader
Заголовки HTTP для передачи с запросом.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TcpProtocol
Переключатель протоколов TCP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidStatusCodeRange
Коды состояния HTTP для успешного рассмотрения. Например, \" 2xx, 301 — 304418 \" .

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorTcpConfiguration

### Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorHttpConfiguration

### Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorIcmpConfiguration

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
