---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: fc94bb7de5663995e75f0c4f1fed05fb36b35f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562928"
---
# Get-AzureRmVpnClientPackage

## КРАТКИй обзор
Получение сведений о пакете VPN-клиента.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmVpnClientPackage** получает сведения о ПАКЕТах VPN-клиентов, доступных на шлюзе виртуальной сети.
Пакеты клиентов содержат данные конфигурации, позволяющие клиентскому компьютеру выполнять VPN-подключение к виртуальной сети Azure; для создания VPN-подключения клиентские компьютеры должны установить правильный пакет конфигурации.
Различные пакеты конфигурации доступны в зависимости от версии Windows на клиентском компьютере (например, Windows 7 или Windows 10) и архитектуры процессора на клиентском компьютере (AMD64 или x86).
При запуске **Get-AzureRmVpnClientPackage** необходимо указать тип архитектуры.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений о пакете клиента для архитектуры процессора VPN
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Эта команда получает сведения о пакетах VPN-клиентов AMD64, хранящихся на виртуальном сетевом шлюзе с именем ContosoVirtualNetworkGateway.
Чтобы получить сведения о пакетах клиентов x86, установите для параметра *processorArchitecture* значение x86.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String
Параметры: ResourceGroupName (ByValue), VirtualNetworkGatewayName (ByValue)

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Изменить размер — AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


