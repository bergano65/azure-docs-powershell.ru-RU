---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517901"
---
# Start-AzVirtualNetworkGatewayConnectionPacketCapture

## SYNOPSIS
Начинается операция захвата пакетов с подключением виртуального сетевого шлюза.

## СИНТАКСИС

### ByName (по умолчанию)
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByInputObject
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Начинается операция захвата пакетов с подключением виртуального сетевого шлюза.

## ПРИМЕРЫ

### Пример 1
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### Пример 2
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### Пример 3
Пример захвата пакетов для захвата внутренних и внешних пакетов
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## PARAMETERS

### -AsJob
Запуск cmdlet в фоновом режиме

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

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilterData
Параметры фильтрации для запуска захвата пакетов при под соединении виртуального сетевого шлюза.

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

### -InputObject
Объект подключения виртуального сетевого шлюза, в котором нужно начать захват пакетов.

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя подключения виртуального сетевого шлюза, в котором нужно начать захват пакетов.

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Azure resource ID of the VirtualNetworkGatewayConnection, в котором нужно начать захват пакетов.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
[Stop-AzVirtualNetworkGatewayConnectionPacketCapture](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)