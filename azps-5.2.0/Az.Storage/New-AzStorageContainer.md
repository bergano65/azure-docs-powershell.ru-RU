---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: b056504786d641d137d5188ed529eecb0ede690f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324789"
---
# New-AzStorageContainer

## SYNOPSIS
Создает контейнер хранилища Azure.

## СИНТАКСИС

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания контейнера хранилища Azure будет создаваться проектлет **New-AzStorageContainer.**

## ПРИМЕРЫ

### Пример 1. Создание контейнера хранилища Azure
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

Эта команда создает контейнер хранилища.

### Пример 2. Создание нескольких контейнеров хранилища Azure
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

В этом примере создается несколько контейнеров хранилища.
Для этого используется **метод разделения** класса .NET **String,** который передает имена в конвейере.

## PARAMETERS

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

### -Контекст
Определяет контекст для нового контейнера.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя нового контейнера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Permission
Определяет уровень общего доступа к этому контейнеру.
По умолчанию доступ к контейнеру и всем его BLOB-сайтам может получить только владелец учетной записи хранения.
Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его BLOB-проекту, можно настроить разрешения для контейнера, чтобы разрешить общедоступный доступ.
Анонимные пользователи могут читать большой объем в общедоступных контейнерах без проверки подлинности запроса.
Допустимые значения этого параметра:
- "Контейнер".
Обеспечивает полный доступ для чтения к контейнеру и его BLOB-лям.
Клиенты могут с помощью анонимного запроса укаймировать в контейнере BLOB-контейнер, но не могут прогонять контейнеры в учетной записи хранения. 
- BLOB.;
Обеспечивает доступ к данным lob-lob во всем контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.
Клиенты не могут с помощью анонимного запроса промерять BLOB-lob-ы в контейнере. 
- "Выключи".
Это ограничение доступа только для владельца учетной записи хранения.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).
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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)

[Set-AzStorageContainerAcl](./Set-AzStorageContainerAcl.md)


