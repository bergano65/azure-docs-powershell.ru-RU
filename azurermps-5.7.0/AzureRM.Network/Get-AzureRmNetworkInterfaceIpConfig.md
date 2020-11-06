---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 3d3185762c6bb60d59ef15a129b4055939b49213
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569931"
---
# Get-AzureRmNetworkInterfaceIpConfig

## КРАТКИй обзор
Возвращает IP-конфигурацию сетевого интерфейса для сетевого интерфейса.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmNetworkInterfaceIPConfig** получает IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.

## ИЛЛЮСТРИРУЮТ

### 1: получение IP-конфигурации сетевого интерфейса
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

Первая команда получает существующий сетевой интерфейс с именем mynic и сохраняет его в переменной $nic 1. Вторая команда возвращает IP-конфигурацию с именем ipconfig1 для этого сетевого интерфейса.
    

## ПАРАМЕТРЫ

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

### -Name (имя)
Указывает имя сетевой IP-конфигурации, которую получает этот командлет.

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

### -NetworkInterface
Указывает объект **NetworkInterface** , который содержит IP-конфигурацию сети, которую получает этот командлет.

```yaml
Type: PSNetworkInterface
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

### PSNetworkInterface
Параметр "NetworkInterface" принимает значение типа "PSNetworkInterface" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmNetworkInterfaceIpConfig](./Add-AzureRmNetworkInterfaceIpConfig.md)

[New-AzureRmNetworkInterfaceIpConfig](./New-AzureRmNetworkInterfaceIpConfig.md)

[Remove-AzureRmNetworkInterfaceIpConfig](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[Set-AzureRmNetworkInterfaceIpConfig](./Set-AzureRmNetworkInterfaceIpConfig.md)


