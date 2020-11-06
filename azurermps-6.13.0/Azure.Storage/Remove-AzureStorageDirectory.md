---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558667"
---
# Remove-AzureStorageDirectory

## КРАТКИй обзор
Удаляет каталог.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Имя_общего_ресурса (по умолчанию)
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Предоставить общий доступ
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Папка
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureStorageDirectory** удаляет каталог.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление папки
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

Эта команда удаляет папку с именем ContosoWorkingFolder из общей папки с именем ContosoShare06.

## ПАРАМЕТРЫ

### -ClientTimeoutPerRequest
Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.
Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.
Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.

```yaml
Type: System.Nullable`1[System.Int32]
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
Type: System.Nullable`1[System.Int32]
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
Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
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

### -Каталог
Определяет папку как объект **CloudFileDirectory** .
Этот командлет удаляет папку, указанную в этом параметре.
Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.
Вы также можете использовать командлет **Get-AzureStorageFile** , чтобы получить доступ к каталогу.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Указывает, что при успешном выполнении командлета возвращается значение $True.
Если указать этот параметр и, если командлет завершился сбоем из-за неприемлемого значения параметра _path_ , командлет возвращает ошибку.
Если этот параметр не указан, этот командлет не возвращает значение.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Указывает путь к папке.
Если папка, в которой указан этот параметр, пуста, этот командлет удаляет эту папку.
Если папка не пустая, этот командлет не вносит никаких изменений и возвращает ошибку.

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Указывает длину тайм-аута для серверной части запроса.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Общий доступ
Указывает объект **CloudFileShare** .
Этот командлет удаляет папку в общей папке, в которой указан этот параметр.
Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.
Этот объект имеет контекст хранилища.
Если вы задаете этот параметр, не указывайте параметр *контекста* .

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Имя_общего_ресурса
Указывает имя общего файлового файла.
Этот командлет удаляет папку в общей папке, в которой указан этот параметр.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Storage. File. CloudFileShare
Параметры: Share (ByValue)

### Microsoft. WindowsAzure. Storage. File. CloudFileDirectory
Параметры: Каталог (ByValue)

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Storage. File. CloudFileDirectory

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)

[New-AzureStorageDirectory](./New-AzureStorageDirectory.md)
