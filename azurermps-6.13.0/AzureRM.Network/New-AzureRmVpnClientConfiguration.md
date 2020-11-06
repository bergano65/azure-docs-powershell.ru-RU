---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: ddd620bb1878106801d6c69c086dc9642e76e1c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566793"
---
# New-AzureRmVpnClientConfiguration

## КРАТКИй обзор
Эта команда позволяет пользователям создавать пакеты профилей VPN на основе предварительно настроенных параметров VPN на шлюзе VPN в дополнение к некоторым дополнительным параметрам, которые может потребоваться настроить пользователи, например некоторые корневые сертификаты.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Это позволит пользователям создавать пакеты профилей VPN на основе предварительно настроенных параметров VPN на шлюзе VPN в дополнение к некоторым дополнительным параметрам, которые может потребоваться настроить пользователи, например, с некоторыми корневыми сертификатами.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Этот командлет используется для создания ZIP-файла профиля клиента VPN для "ContosoVirtualNetworkGateway" в ResourceGroup "ContosoResourceGroup". Профиль создается для предварительно настроенного сервера RADIUS, который настроен на использование метода проверки подлинности "EAPTLS" с файлом сертификата VpnProfileRadiusCert.

## ПАРАМЕТРЫ

### -AuthenticationMethod
Метод проверки подлинности может принимать значения EAPMSCHAPv2 или EAPTLS. Если указан EAPMSCHAPv2, командлет создает установщик конфигурации клиента для проверки подлинности имени пользователя и пароля, использующего протокол проверки подлинности EAP-MSCHAPv2. Если указан EAPTLS, командлет создает установщик конфигурации клиента для проверки подлинности сертификата, использующей протокол EAP-TLS. Параметр "EapTls" можно использовать как для проверки подлинности сертификата на основе RADIUS, так и для проверки подлинности сертификации, выполненной виртуальным сетевым шлюзом, загрузя доверенный корневой каталог. Командлет автоматически определяет, что настроено.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Список путей к корневому сертификату клиента

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name (имя)
Название ресурса.

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

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Путь корневого сертификата RADIUS-сервера. Это обязательный параметр, который должен быть указан при использовании EAP-TLS с проверкой подлинности RADIUS. Это полный путь CER-файла, содержащего корневой сертификат RADIUS, который используется клиентом для проверки RADIUS-сервера во время проверки подлинности.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVpnProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
