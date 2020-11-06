---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66845678619a7777bbda9257aa208393b0fa178c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556271"
---
# Get-AzureStorageContainer

## КРАТКИй обзор
Список контейнеров хранилища.

## Максимальное

### ContainerName (по умолчанию)
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPrefix
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение блоба хранилища Azure по имени
```
PS C:\>Get-AzureStorageContainer -Name container*
```

В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.

### Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.

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
Указывает контекст хранилища.
Чтобы создать его, можно использовать командлет New-AzureStorageContext.

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

### -ContinuationToken
Указывает маркер продолжения для списка больших двоичных объектов.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Задает максимальное количество объектов, возвращаемых этим командлетом.

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

### -Name (имя)
Указывает имя контейнера.
Если имя контейнера пусто, командлет выводит список всех контейнеров.
В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix (префикс)
Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.
Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Указывает интервал времени ожидания службы (в секундах) для запроса.
Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.

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

[New-AzureStorageContainer](./New-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)

[Set-AzureStorageContainerAcl](./Set-AzureStorageContainerAcl.md)


