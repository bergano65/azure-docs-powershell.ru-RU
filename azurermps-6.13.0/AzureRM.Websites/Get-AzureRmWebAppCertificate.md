---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: 94cd9c6aa3c47d87b1c99a1f8ae68c48c613aefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562499"
---
# Get-AzureRmWebAppCertificate

## КРАТКИй обзор
Получает сертификат веб-приложения Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmWebAppCertificate** получает сведения о сертификатах веб-приложения Azure, связанных с определенной группой ресурсов.
Если вы знаете отпечаток сертификата, вы также можете использовать этот командлет для получения сведений об указанном сертификате.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сертификатов веб-приложения в группе ресурсов
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

Эта команда возвращает сведения о загруженных сертификатах веб-приложения, связанных с группой ресурсов ContosoResourceGroup.

### Пример 2: получение указанного сертификата веб-приложения
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Эта команда получает сертификат веб-приложения ContosoResourceGroup с отпечатком E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.

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
Указывает имя группы ресурсов, которой назначен сертификат.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отпечаток
Указывает уникальный идентификатор сертификата.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. website. Models. Certificate

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)


