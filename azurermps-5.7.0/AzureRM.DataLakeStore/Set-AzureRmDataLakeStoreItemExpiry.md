---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567015"
---
# Set-AzureRmDataLakeStoreItemExpiry

## КРАТКИй обзор
Задает или удаляет время окончания срока действия файла в учетной записи Azure Data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### SetAbsoluteNeverExpireExpiry (по умолчанию)
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRelativeExpiry
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmDataLakeStoreItemExpiry** задает или удаляет время окончания для файла в учетной записи Azure Data Lake Store.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Установка срока действия для файла
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Задает срок действия файла в myfile.txt учетной записи в ContosoADL в два часа.
Это приведет к истечении срока действия файла (помечается для удаления) в два часа.

### Пример 2: удаление срока действия для файла
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

Удаление срока действия, установленного ранее, для файла "myfile.txt" в учетной записи "ContosoADL".
Это означает, что срок действия файла не истечет автоматически (помечать для удаления), и его необходимо будет удалить вручную или установить срок действия.


### Пример 3: Настройка срока действия файла относительно текущего времени
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

Первая команда задает время истечения срока действия файла/myfile.txt 240 секунды относительно текущего времени на сервере.

Вторая команда задает время истечения срока действия файла/myfile.txt 240 секунд относительно времени создания на сервере.

## ПАРАМЕТРЫ

### -Account (учетная запись)
Указывает имя учетной записи Data Lake Store.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Срок действия
Абсолютное время окончания срока действия указанного файла.
Если значение не указано или равно MaxValue, срок действия файла не ограничен.

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Относительные параметры срока действия. RelativeToNow или RelativeToCreationDate являются текущими параметрами
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Задает путь к файлу Data Lake Store для элемента, для которого нужно задать или удалить срок действия.

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeTime
Относительное время (в миллисекундах), по отношению к моменту и времени создания
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### DataLakeStoreItem
Обновленный файл с новым временем истечения срока действия.

## Пуск
Alias (псевдоним): Set-AdlStoreItemExpiry

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

