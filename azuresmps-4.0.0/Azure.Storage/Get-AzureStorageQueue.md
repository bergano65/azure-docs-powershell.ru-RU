---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556255"
---
# Get-AzureStorageQueue

## КРАТКИй обзор
Выводит список очередей хранилища.

## Максимальное

### QueueName (по умолчанию)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageQueue** перечисляет очереди хранения, связанные с учетной записью хранения Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех очередей хранилища Azure
```
PS C:\>Get-AzureStorageQueue
```

Эта команда возвращает список всех очередей хранилища для текущей учетной записи хранения.

### Пример 2: список очередей хранилища Azure с использованием подстановочных знаков
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Эта команда использует подстановочный знак для получения списка очередей хранилища, имя которого начинается с очереди.

### Пример 3: список очередей хранилища Azure с использованием префикса имени очереди
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

В этом примере используется параметр *prefix* для получения списка очередей хранилища, имена которых начинаются с очереди.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Вы можете создать его с помощью командлета **New-AzureStorageContext** .

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
Задает имя.
Если имя не указано, командлет возвращает список всех очередей.
Если указано полное или частичное имя, командлет получает все очереди, соответствующие шаблону имени.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix (префикс)
Задает префикс, используемый в именах очередей, которые вы хотите получить.

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
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

[New-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


