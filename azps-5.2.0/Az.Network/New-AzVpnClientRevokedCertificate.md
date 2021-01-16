---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406231"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Создание нового сертификата vpn-отзыва клиента.

## СИНТАКСИС

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для использования виртуального сетевого шлюза с помощью нового сертификата отзыва клиента в **AzVpnClientRevokedCertificate** создается новый сертификат отзыва клиента виртуальной частной сети (VPN).
Сертификаты отзыва клиента не могут использовать указанный сертификат для проверки подлинности.
Этот cmdlet создает автономный сертификат, который не назначен виртуальному шлюзу.
Вместо этого сертификат, созданный **new-AzVpnClientRevokedCertificate,** используется в сочетании с New-AzVirtualNetworkGateway при создании нового шлюза.
Предположим, например, что вы создали новый сертификат и храните его в переменной с $Certificate.
Этот объект сертификата можно использовать при создании нового виртуального шлюза.
Например, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Дополнительные сведения см. в документации New-AzVirtualNetworkGateway управления проектами.

## ПРИМЕРЫ

### Пример 1. Создание отозванного сертификата клиента
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Эта команда создает новый отозванный клиентом сертификат и сохраняет объект сертификата в переменной с именем $Certificate.
Затем с помощью **командлета New-AzVirtualNetworkGateway** можно добавить сертификат к новому виртуальному сетевому шлюзу.

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

### -Name
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

### -Thumbprint
Указывает уникальный идентификатор добавляемого сертификата.
Получить сведения о эскизах для сертификатов можно с помощью команды Windows PowerShell примерно так: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Предшествуя команда возвращает сведения для всех сертификатов локального компьютера, найденных в хранилище корневых сертификатов.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


