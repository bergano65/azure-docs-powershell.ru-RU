---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558672"
---
# New-AzureStorageTable

## КРАТКИй обзор
Создание таблицы хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageTable** создает таблицу хранилища, связанную с учетной записью хранения в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание таблицы хранилища Azure
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

Эта команда создает таблицу хранилища с именем tableabc.

### Пример 2: создание нескольких таблиц хранилища Azure
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

Эта команда создает несколько таблиц.
Он использует метод **Split** класса **String** .NET и передает имена в конвейере.

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
Задает имя новой таблицы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


