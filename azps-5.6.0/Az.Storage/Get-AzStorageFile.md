---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: e61171faba3661ad1d518641655ad87f06771ae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997097"
---
# Get-AzStorageFile

## SYNOPSIS
Список каталогов и файлов для пути.

## СИНТАКСИС

### ShareName (по умолчанию)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Предоставить общий доступ
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Каталог
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для задаваемого вами списка каталогов и файлов для задаваемой папки **Get-AzStorageFile** будет указано ее каталог.
Укажите *параметр Path,* чтобы получить экземпляр каталога или файла в указанном пути.
Этот cmdlet возвращает **объекты AzureStorageFile** и **AzureStorageDirectory.**
С помощью свойства **IsDirectory можно** различать папки и файлы.

## ПРИМЕРЫ

### Пример 1. Список каталогов в области
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

Эта команда содержит только каталоги в share ContosoShare06.
Он сначала извлекает файлы и каталоги,  передает их в оператор конвейера, а затем удаляет объекты, тип которых не "AzureStorageFileDirectory".

### Пример 2. Список каталогов файлов
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Эта команда содержит список файлов и папок в папке ContosoWorkingFolder каталога ContosoShare06.
Сначала он получает экземпляр каталога, а затем перена каналает его в список каталогов с cmdlet **Get-AzStorageFile.**

## PARAMETERS

### -ClientTimeoutPerRequest
Указывает интервал времени времени клиентского времени (в секундах) для одного запроса на обслуживание.
Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.
Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Указывает максимальное число сетевых звонков.
С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.
Указанное значение является абсолютным и не умножается на основное.
Этот параметр помогает устранять проблемы с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.
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

### -Контекст
Указывает контекст хранилища Azure.
Чтобы получить контекст хранилища, воспользуйтесь New-AzStorageContext управления.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Каталог
Указывает папку как объект **CloudFileDirectory.**
Этот cmdlet возвращает папку, указанную этим параметром.
Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.
Для получения каталога также можно использовать **cmdlet Get-AzStorageFile.**

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Path
Путь к папке.
Если опустить параметр *Path,* **Get-AzStorageFile** выведет список каталогов и файлов в указанной папке или каталоге.
Если включить параметр *Path,* **Get-AzStorageFile** возвращает экземпляр каталога или файла, указанный по указанному пути.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Указывает для запроса интервал времени в секундах на стороне службы.
Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Share
Указывает объект **CloudFileShare.**
Этот cmdlet получает файл или каталог из файловой папки, указанной этим параметром.
Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.
Этот объект содержит контекст хранилища.
Если вы указали этот параметр, не укажите параметр *Context.*

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
Имя файловой папки.
Этот cmdlet получает файл или каталог из файловой папки, указанной этим параметром.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


