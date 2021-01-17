---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422004"
---
# Get-AzVpnClientRootCertificate

## SYNOPSIS
Сведения о корневых сертификатах VPN.

## СИНТАКСИС

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzVpnClientRootCertificate** возвращает сведения о корневых сертификатах, которые назначены виртуальному сетевому шлюзу.
Корневые сертификаты — это сертификаты X.509, которые определяют корневой сертификат сертификации: все остальные сертификаты, используемые на шлюзе, доверять корневому сертификату.
По умолчанию **Get-AzVpnClientRootCertificate** возвращает сведения обо всех корневых сертификатах, которые назначены шлюзу.
(Шлюзы могут иметь несколько корневых сертификатов.) Однако включив параметр **VpnClientRootCertificateName,** вы можете ограничить возвращаемую информацию определенным сертификатом.

## ПРИМЕРЫ

### Пример 1. Сведения обо всех корневых сертификатах
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

Эта команда получает сведения обо всех корневых сертификатах, которые назначены виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.

### Пример 2. Просмотр сведений о конкретных корневых сертификатах
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

Эта команда является вариантом команды, показанной в примере 1.
Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемую информацию определенным корневым сертификатом: ContosoRootClientCertificate.

## PARAMETERS

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

### -ResourceGroupName
Указывает имя группы ресурсов, которая назначена виртуальному сетевому шлюзу.
Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.

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
Указывает имя виртуального сетевого шлюза, корневого сертификата которого назначен.

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
Указывает имя корневого сертификата клиента, который получает этот cmdlet.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


