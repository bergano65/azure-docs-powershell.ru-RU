---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: fdd7a7c655b46eb3fc1ca8673fb8fb5f36dcd850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561296"
---
# Get-AzureStorageServiceMetricsProperty

## КРАТКИй обзор
Возвращает свойства метрик для службы хранилища Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение свойств метрик для службы больших двоичных объектов
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -MetricsType
Указывает тип метрики.
Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.
Допустимые значения этого параметра: hours и Minute.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Указывает тип службы хранилища.
Этот командлет получает свойства метрик для типа, который указывает этот параметр.
Для этого параметра допустимы следующие значения:
- Большом 
- Таблич
- Поместить
- Файл. значение файла в настоящее время не поддерживается.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


