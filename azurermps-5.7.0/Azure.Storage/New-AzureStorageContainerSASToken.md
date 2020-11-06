---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
ms.openlocfilehash: 0e8ad44ebbd8a5585626de27317caa14b408f87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567035"
---
# New-AzureStorageContainerSASToken

## КРАТКИй обзор
Создание маркера SAS для контейнера хранилища Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### SasPolicy
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageContainerSASToken** создает маркер подписи общего доступа (SAS) для контейнера хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание маркера безопасности контейнера с разрешениями полного контейнера
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

В этом примере создается маркер безопасности контейнера с разрешениями полного контейнера.

### Пример 2: создание маркера SAS с несколькими контейнерами с помощью конвейера
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

В этом примере создается несколько маркеров сопоставления безопасности контейнера с помощью конвейера.

### Пример 3: создание маркера SAS контейнера с политикой общего доступа
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

В этом примере создается маркер SAS контейнера с политикой общего доступа.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Вы можете создать его с помощью командлета New-AzureStorageContext.

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

Если пользователь задает время начала, но не время окончания срока действия, в качестве времени окончания устанавливается время начала плюс один час.
Если не задано ни время начала, ни время окончания срока действия, в качестве времени окончания устанавливается текущее время плюс один час.

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

### -FullUri
Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.

```yaml
Type: SwitchParameter
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

### -Name (имя)
Указывает имя контейнера хранилища Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Разрешения
Задает разрешения для контейнера хранилища.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy (политика)
Указывает политику сохраненного доступа Azure.

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (протокол)
Указывает протокол, разрешенный для запроса.
Для этого параметра допустимы следующие значения:
* HttpsOnly
* HttpsOrHttp

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

### -StartTime
Задает время, в течение которого подпись общего доступа становится действительной.

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

### Подстрок

Параметр Name принимает значение типа String из конвейера.

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)
