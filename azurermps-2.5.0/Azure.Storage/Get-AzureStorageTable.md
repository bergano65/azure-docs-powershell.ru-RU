---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 834400893dc3d2065a8ca3f0b27783e0a4d5604e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914309"
---
# Get-AzureStorageTable

## КРАТКИй обзор
Список таблиц хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### TableName (по умолчанию)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageTable** перечисляет таблицы хранения, связанные с учетной записью хранения в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех таблиц хранилища Azure
```
PS C:\>Get-AzureStorageTable
```

Эта команда получает все таблицы хранилища для учетной записи хранения.

### Пример 2: список таблиц хранилища Azure с использованием подстановочных знаков
```
PS C:\>Get-AzureStorageTable -Name table*
```

Эта команда использует подстановочный знак для получения таблиц хранилища, имя которых начинается с Table.

### Пример 3: список таблиц хранилища Azure с использованием префикса имени таблицы
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Эта команда использует параметр *prefix* для получения таблиц хранилища, имя которых начинается с Table.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища.
Чтобы создать его, можно использовать командлет New-AzureStorageContext.

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

### -Name (имя)
Указывает имя таблицы.
Если имя таблицы пусто, командлет выводит список всех таблиц.
В противном случае выводится список всех таблиц, соответствующих указанному имени или шаблону обычного имени.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix (префикс)
Задает префикс, используемый в имени таблицы или таблиц, которые требуется получить.
Вы можете использовать этот параметр, чтобы найти все таблицы, которые начинаются с одной строки, например Table.

```yaml
Type: System.String
Parameter Sets: TablePrefix
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


