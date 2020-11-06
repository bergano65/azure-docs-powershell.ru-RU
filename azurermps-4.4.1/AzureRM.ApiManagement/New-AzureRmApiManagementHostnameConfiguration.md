---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565729"
---
# New-AzureRmApiManagementHostnameConfiguration

## КРАТКИй обзор
Создает экземпляр PsApiManagementHostnameConfiguration.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmApiManagementHostnameConfiguration** является вспомогательной командой, которая создает экземпляр **PsApiManagementHostnameConfiguration**.
Эта команда используется с командлетом Set-AzureRmApiManagementHostnames.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание и инициализация экземпляра PsApiManagementHostnameConfiguration
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

Эта команда создает и инициализирует экземпляр **PsApiManagementHostnameConfiguration**.

## ПАРАМЕТРЫ

### -CertificateThumbprint
Указывает отпечаток сертификата.
Сертификат необходимо сначала импортировать с помощью командлета Import-AzureRmApiManagementHostnameCertificate.

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

### -Hostname
Задает настраиваемое имя узла, для которого этот командлет создает экземпляр **PsApiManagementHostnameConfiguration** .

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

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Import-AzureRmApiManagementHostnameCertificate](./Import-AzureRmApiManagementHostnameCertificate.md)

[Set-AzureRmApiManagementHostnames](./Set-AzureRmApiManagementHostnames.md)


