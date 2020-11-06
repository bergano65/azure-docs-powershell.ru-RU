---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 6303aeac769b2303e8ebbd67a237d2eaf99ed9cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562907"
---
# Get-AzureRmVpnClientRootCertificate

## КРАТКИй обзор
Получение сведений о корневых сертификатах VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmVpnClientRootCertificate** возвращает сведения о корневых сертификатах, назначенных шлюзу виртуальной сети.
Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.
По умолчанию **Get-AzureRmVpnClientRootCertificate** возвращает сведения о всех корневых сертификатах, назначенных шлюзу.
(Шлюзы могут иметь более одного корневого сертификата.) Однако, включив параметр **VpnClientRootCertificateName** , вы можете ограничить возвращаемые данные определенным сертификатом.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех корневых сертификатах
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

Эта команда получает сведения обо всех корневых сертификатах, назначенных виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.

### Пример 2: получение сведений о конкретных корневых сертификатах
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

Эта команда является вариантом команды, показанной в примере 1.
Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемые данные определенным корневым сертификатом: ContosoRootClientCertificate.

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Указывает имя шлюза виртуальной сети, на котором назначен корневой сертификат.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificateName
Указывает имя корневого сертификата клиента, который получает этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

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

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[New-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)

[Remove-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


