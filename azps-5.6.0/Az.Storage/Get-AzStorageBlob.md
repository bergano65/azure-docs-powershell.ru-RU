---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 317d25ecfa48203c411f368aa5b00ac3380773ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002760"
---
# Get-AzStorageBlob

## SYNOPSIS
Список BLOB-то в контейнере.

## СИНТАКСИС

### BlobName (по умолчанию)
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### SingleBlobSnapshotTime
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### SingleBlobVersionID
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## ОПИСАНИЕ
С его учетной записью в учетной записи хранилища Azure в списке **BLOB-хранилищ в Get-AzStorageBlob** перечислены BLOB-клиенты в указанном контейнере.

## ПРИМЕРЫ

### Пример 1. Получить большой бизнес-бизнес по имени
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

Эта команда использует имя BLOB-ля и поддиавный знак для его получения.

### Пример 2. В контейнере можно получать большой объем в контейнере с помощью конвейера
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

Эта команда использует канал для получения всех BLOB-проектов (включая их в состоянии "Удаленные") в контейнер.

### Пример 3. Получить BLOB-бизнес по префиксу имени
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

Для этого используется префикс имени.

### Пример 4. Список BLOB-залов в нескольких пакетах
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

В этом примере *параметры MaxCount* и *ContinuationToken* используются для списка BLOB-залов хранилища Azure в нескольких пакетах.
Первые четыре команды присваивают значения переменным, которые используются в примере.
Пятая команда указывает на утверждение **Do-While,** использующее командлет **Get-AzStorageBlob** для получения BLOB-ей части.
Она включает маркер продолжения, который хранится в переменной $Token продолжения.
$Token изменяет значение по мере его цикла.
Для получения дополнительных сведений введите `Get-Help About_Do` .
Для отображения итогового числа в конечной команде используется команда **Echo.**

### Пример 5. Все BLOB-lob-lob в контейнере включают версию BLOB-lob
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

Эта команда получает все BLOB-lob-lob в контейнере, включая версию BLOB-lob.

### Пример 6. Получить одну версию BLOB-lob
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

Эта команда получает одну вершину BLOB-команд с VersionId.

### Пример 7. Получить один моментальный снимок BLOB-бизнеса
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

Эта команда получает один моментальный снимок большой lob-lob-2016 с помощью Моментального времени.

## PARAMETERS

### -BLOB
Определяет имя или шаблон имени, который можно использовать для поиска поддерев.
Если имя BLOB-ля не задано, будет выдан список всех BLOB-имен в этом контейнере.
Если для этого параметра задано значение, командлет перечисляет все BLOB-lob-группы с именами, которые соответствуют этому параметру. Этот параметр поддерживает поддиавные знаки в любом месте строки.

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.
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
Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.
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

### -Container
Имя контейнера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Контекст
Указывает учетную запись хранилища Azure, из которой вы хотите получить список BLOB-хранилищ.
С помощью New-AzStorageContext можно создать контекст хранилища.

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

### -ContinuationToken
Указывает маркер продолжения для списка BLOB-приложений.
Используйте этот параметр и параметр *MaxCount* для списка BLOB-залов в нескольких пакетах.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -IncludeDeleted
Include Deleted BLOB, по умолчанию он не включает удаленный BLOB-ля.

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

### -IncludeVersion
Версии BLOB-параметров будут перечислены только в том случае, если этот параметр присутствует, по умолчанию они не включают BLOB-версии.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Указывает максимальное количество объектов, возвращаемых этим cmdlet.

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

### -Префикс
Указывает префикс для имен BLOB-имен, которые вы хотите получить.
Этот параметр не поддерживает использование регулярных выражений или поддикт-знаков для поиска.
Это означает, что если в контейнере есть только BLOB-lob-группы "Мой", "МойBlob1" и "MyBlob2" и вы указали "-Prefix My*", cmdlet returns no blobs.
Однако если указать "-Префикс Мой", будет возвращены "Мой", "МойBlob1" и "MyBlob2".

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Для запроса указывается интервал времени, заданный для времени отрезка времени для стороны обслуживания (в секундах).
Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.

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

### -SnapshotTime
Blob SnapshotTime

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionId
Blob VersionId

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageBlobContent](./Get-AzStorageBlobContent.md)

[Remove-AzStorageBlob](./Remove-AzStorageBlob.md)

[Set-AzStorageBlobContent](./Set-AzStorageBlobContent.md)


