---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555796"
---
# New-AzureStorageShareSASToken

## КРАТКИй обзор
Создание маркера подписи общего доступа для общей папки хранилища Azure.

## Максимальное

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageShareSASToken** создает маркер подписи для общего доступа к хранилищу Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание маркера цифровой подписи для общего доступа
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

Эта команда создает маркер подписи общего доступа для общей папки с именем ContosoShare.

### Пример 2: создание нескольких маркеров общего доступа к подписи с помощью конвейера
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

Эта команда получает все общие ресурсы хранилища, соответствующие проверке префикса.
Команда передает их в текущий командлет с помощью оператора конвейера.
Текущий командлет создает маркер общего доступа для каждой общей папки хранения с указанными разрешениями.

### Пример 3: создание маркера подписи общего доступа, использующего политику общего доступа
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

Эта команда создает маркер подписи общего доступа для общей папки хранения с именем ContosoShare, имеющей политику с именем ContosoPolicy03.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Чтобы получить контекст, используйте командлет New-AzureStorageContext.

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

### -Разрешения
Задает разрешения в маркере для доступа к общему доступу и файлам в общем доступе.

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
Указывает политику сохраненных прав доступа для общего доступа.

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

### -Имя_общего_ресурса
Указывает имя общего доступа к хранилищу.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

## НАПРЯЖЕНИЕ

## Пуск
* Ключевые слова: общие, Azure, службы, данные, хранилище, большой двоичный объект, очередь, таблица

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
