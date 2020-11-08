---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064832"
---
# Get-AzVpnClientPackage

## КРАТКИй обзор
Получение сведений о пакете VPN-клиента.

## Максимальное

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzVpnClientPackage** получает сведения о ПАКЕТах VPN-клиентов, доступных на шлюзе виртуальной сети.
Пакеты клиентов содержат данные конфигурации, позволяющие клиентскому компьютеру выполнять VPN-подключение к виртуальной сети Azure; для создания VPN-подключения клиентские компьютеры должны установить правильный пакет конфигурации.
Различные пакеты конфигурации доступны в зависимости от версии Windows на клиентском компьютере (например, Windows 7 или Windows 10) и архитектуры процессора на клиентском компьютере (AMD64 или x86).
При запуске **Get-AzVpnClientPackage** необходимо указать тип архитектуры.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений о пакете клиента для архитектуры процессора VPN
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Эта команда получает сведения о пакетах VPN-клиентов AMD64, хранящихся на виртуальном сетевом шлюзе с именем ContosoVirtualNetworkGateway.
Чтобы получить сведения о пакетах клиентов x86, установите для параметра *processorArchitecture* значение x86.

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

### -ProcessorArchitecture
Указывает тип архитектуры ЦП, для которой предназначен клиентский пакет.
Допустимые значения: AMD64 и x86.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.
Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Указывает имя шлюза виртуальной сети, в котором хранятся сведения о клиентском пакете.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Изменить размер — AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


