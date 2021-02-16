---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406848"
---
# Get-AzVpnClientPackage

## SYNOPSIS
Сведения о пакете клиента VPN.

## СИНТАКСИС

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet get-AzVpnClientPackage** можно получить сведения о пакетах клиента VPN, которые доступны для виртуального сетевого шлюза.
Пакеты клиента содержат данные конфигурации, позволяющие клиентский компьютеру использовать VPN-подключение к виртуальной сети Azure; Чтобы установить VPN-подключение, на клиентских компьютерах должен быть установлен правильный пакет конфигурации.
Доступные пакеты конфигурации основаны на версии Windows клиентского компьютера (например, Windows 7 или Windows 10) и архитектуре процессора клиентского компьютера (AMD64 или x86).
Тип архитектуры необходимо указать при запуске **Get-AzVpnClientPackage.**

## ПРИМЕРЫ

### Пример 1. Сведения о пакете клиента VPN для процессоров
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Эта команда получает сведения о пакетах клиента AMD64 VPN, которые хранятся в виртуальном сетевом шлюзе ContosoVirtualNetworkGateway.
Чтобы получить сведения о пакетах клиента x86, установите для параметра *ProcessorArchitecture* значение x86.

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

### -ProcessorArchitecture
Определяет тип архитектуры ЦП, для которую предназначен пакет клиента.
Допустимые значения: Amd64 и X86.

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
Указывает имя группы ресурсов, которая назначена виртуальному сетевому шлюзу.
Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.

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
Указывает имя виртуального сетевого шлюза, в котором хранится информация о пакете клиента.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)



