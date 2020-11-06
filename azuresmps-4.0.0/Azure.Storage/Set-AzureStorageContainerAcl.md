---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa33f6ba457ad51504cc9005f70f0e4c8f529359
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556364"
---
# Set-AzureStorageContainerAcl

## КРАТКИй обзор
Задает разрешение Public Access для контейнера хранилища.

## Максимальное

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureStorageContainerAcl** задает разрешение Public Access указанному контейнеру хранилища в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка ACL контейнера хранилища Azure по имени
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

Эта команда создает контейнер, у которого нет общедоступного доступа.

### Пример 2: Настройка ACL контейнера хранилища Azure с помощью конвейера
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

Эта команда получает все контейнеры хранилища с именем, начинающимся с Container, и передает результат в конвейер, чтобы установить для него разрешение на доступ ко всем двоичным объектам.

## ПАРАМЕТРЫ

### -ClientTimeoutPerRequest
Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.
Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.
Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Задает максимальное количество одновременных сетевых вызовов.
Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.
Указанное значение является абсолютным числом и не умножается на количество ядер.
Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.
Значение по умолчанию — 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Name (имя)
Указывает имя контейнера.

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

### -PassThru
Возвращает объект, который представляет собой элемент, с которым вы работаете.
По умолчанию этот командлет не создает никаких выходных данных.

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

### -Разрешения
Указывает уровень общедоступного доступа к этому контейнеру.
По умолчанию контейнер и любые большие двоичные объекты в нем могут быть доступны только владельцу учетной записи хранения.
Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его больших двоичных объектов, вы можете задать разрешения на доступ к контейнеру, чтобы включить общий доступ.
Анонимные пользователи могут читать большие двоичные объекты в общедоступном контейнере без проверки подлинности запроса.
Для этого параметра допустимы следующие значения:

--Контейнер.
Предоставляет полный доступ на чтение для контейнера и его больших двоичных объектов.
Клиенты могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса, но не могут перечислять контейнеры в учетной записи хранения. --BLOB.
Предоставляет доступ на чтение к данным BLOB-объектов в контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.
Клиенты не могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса. -Отключение.
Ограничивает доступ только владельцам учетной записи хранения.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Указывает интервал времени ожидания службы (в секундах) для запроса.
Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.
Время на стороне сервера для каждого запроса.

```yaml
Type: Int32
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

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[New-AzureStorageContainer](./New-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)


