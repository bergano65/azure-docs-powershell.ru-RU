---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: c55fb1af95b1c0f85e2b36732f6235ad0c6c78d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909797"
---
# Get-AzVpnClientRootCertificate

## КРАТКИй обзор
Получение сведений о корневых сертификатах VPN.

## Максимальное

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzVpnClientRootCertificate** возвращает сведения о корневых сертификатах, назначенных шлюзу виртуальной сети.
Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.

По умолчанию **Get-AzVpnClientRootCertificate** возвращает сведения о всех корневых сертификатах, назначенных шлюзу.
(Шлюзы могут иметь более одного корневого сертификата.) Однако, включив параметр **VpnClientRootCertificateName** , вы можете ограничить возвращаемые данные определенным сертификатом.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех корневых сертификатах
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

Эта команда получает сведения обо всех корневых сертификатах, назначенных виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.

### Пример 2: получение сведений о конкретных корневых сертификатах
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

Эта команда является вариантом команды, показанной в примере 1.
Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемые данные определенным корневым сертификатом: ContosoRootClientCertificate.

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

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.

Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.

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

### -VirtualNetworkGatewayName
Указывает имя шлюза виртуальной сети, на котором назначен корневой сертификат.

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

### -VpnClientRootCertificateName
Указывает имя корневого сертификата клиента, который получает этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

###  
**Get-AzVpnClientRootCertificate** получает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


