---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559663"
---
# New-AzureRmVpnClientRevokedCertificate

## КРАТКИй обзор
Создание нового сертификата отзыва VPN-клиента.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmVpnClientRevokedCertificate** создает новый сертификат отзыва для клиента виртуальной частной сети (VPN) для использования на шлюзе виртуальной сети.
Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.

Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.
Вместо этого сертификат, созданный с помощью **New-AzureRmVpnClientRevokedCertificate** , используется вместе с командлетом New-AzureRmVirtualNetworkGateway при создании нового шлюза.
Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.
Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.
Например,

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

Дополнительные сведения можно найти в документации по командлету New-AzureRmVirtualNetworkGateway.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание нового сертификата, отозванного клиентом
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Эта команда создает новый сертификат, отозванный клиентом, и сохраняет объект сертификата в переменной с именем $Certificate.
Эта переменная может затем использоваться командлетом **New-AzureRmVirtualNetworkGateway** для добавления сертификата в новый шлюз виртуальной сети.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает уникальное имя для нового сертификата отзыва клиента.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отпечаток
Указывает уникальный идентификатор добавляемого сертификата.

Вы можете вернуть отпечаток для сертификатов с помощью команды Windows PowerShell, как показано ниже:

`Get-ChildItem -Path Cert:\LocalMachine\Root`

Предыдущая команда возвращает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
Этот командлет не поддерживает конвейерный вход.

## НАПРЯЖЕНИЕ

###  
Этот командлет создает новые экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


