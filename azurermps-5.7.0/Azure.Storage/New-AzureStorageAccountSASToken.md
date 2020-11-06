---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567037"
---
# New-AzureStorageAccountSASToken

## КРАТКИй обзор
Создание маркера SAS на уровне учетной записи.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageSASToken** создает маркер подписи общего доступа (SAS) для учетной записи хранения Azure на уровне учетной записи.

Вы можете использовать маркер SAS для делегирования разрешений для нескольких служб или делегирования разрешений для служб, недоступных с маркером SAS уровня объекта.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание маркера SAS уровня учетной записи с полным разрешением
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Эта команда создает маркер SAS уровня учетной записи с полным разрешением.

### Пример 2: создание маркера SAS уровня учетной записи для диапазона IP-адресов
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Эта команда создает маркер SAS уровня учетной записи для запросов HTTPS с указанным диапазоном IP-адресов.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Вы можете использовать командлет New-AzureStorageContext, чтобы получить объект **AzureStorageContext** .

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Задает время, по истечении которого подпись общего доступа становится недействительной.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).
Диапазон — включительно.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Разрешения
Задает разрешения для учетной записи хранения.
Разрешения действительны только в том случае, если они соответствуют указанному типу ресурсов.
Дополнительные сведения о допустимых значениях разрешений можно найти в разделе Создание SAS для учетной записиhttps://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (протокол)
Указывает протокол, разрешенный для запроса, созданного с помощью сопоставлений безопасности учетной записи.
Для этого параметра допустимы следующие значения:

- HttpsOnly
- HttpsOrHttp

Значением по умолчанию является HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Указывает типы ресурсов, доступные в токене SAS.
Для этого параметра допустимы следующие значения:

- Ничего
- Сервиса
- Контейнер
- DataObject

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Служба
Указывает службу.
Для этого параметра допустимы следующие значения:

- Ничего
- Большом
- Файл
- Поместить
- Таблич

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Указывает время в виде объекта **DateTime** , в котором SA становится действительной.
Чтобы получить объект **DateTime** , используйте командлет Get-Date.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### IStorageContext

Параметр "Context" принимает значение типа "IStorageContext" из конвейера.

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[New-AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[New-AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


