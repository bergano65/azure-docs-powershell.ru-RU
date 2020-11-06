---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558756"
---
# Get-AzureRmStorageAccount

## КРАТКИй обзор
Получение учетной записи хранения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ResourceGroupParameterSet
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmStorageAccount** получает указанную учетную запись хранения или все учетные записи хранения в группе ресурсов или подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение указанной учетной записи хранения
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Эта команда получает указанную учетную запись хранения.

### Пример 2: получение всех учетных записей хранения в группе ресурсов
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

Эта команда получает все учетные записи хранения в группе ресурсов.

### Пример 3: получение всех учетных записей хранения в подписке
```
PS C:\>Get-AzureRmStorageAccount
```

Эта команда получает все учетные записи хранения в подписке.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя учетной записи хранения, которое требуется получить.

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую требуется получить.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
