---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002264"
---
# Set-AzStorageContainerAcl

## SYNOPSIS
Задает разрешение на общедоступный доступ для контейнера хранилища.

## СИНТАКСИС

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Set-AzStorageContainerAcl** задает разрешение на общедоступный доступ для указанного контейнера хранилища в Azure.

## ПРИМЕРЫ

### Пример 1. Настройка ACL контейнера хранилища Azure по имени
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

Эта команда создает контейнер, не доступный всем.

### Пример 2. Настройка ACL контейнера хранилища Azure с помощью конвейера
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

Эта команда получает все контейнеры хранилища, имя которых начинается с контейнера, а затем передает результат в конвейере, чтобы установить для них разрешение на доступ к BLOB-проекту.

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
Указывает максимальное число сетевых звонков одновременно.
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
Определяет контекст хранилища Azure.
Его можно создать с помощью New-AzStorageContext-управления.

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
Имя контейнера.

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

### -PassThru
Возвращает объект, представляющий элемент, с которым вы работаете.
По умолчанию этот cmdlet не создает никаких выходных данных.

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

### -Permission
Определяет уровень общего доступа к этому контейнеру.
По умолчанию доступ к контейнеру и всем его BLOB-сайтам может получить только владелец учетной записи хранения.
Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его BLOB-контейнера, можно настроить разрешения на доступ к контейнеру для общего доступа.
Анонимные пользователи могут читать большой объем в общедоступных контейнерах без проверки подлинности запроса.
Допустимые значения для этого параметра: --Container.
Обеспечивает полный доступ для чтения к контейнеру и его BLOB-лям.
Клиенты могут с помощью анонимного запроса укаймировать в контейнере BLOB-контейнер, но не могут продумыть контейнеры в учетной записи хранения. --BLOB.)
Обеспечивает доступ считываемой информации в контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.
Клиенты не могут с помощью анонимного запроса укаймировать BLOB-клиенты в контейнере. --Выключите.
Ограничивает доступ только к учетной записи хранения.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).
Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.
Время времени, не в течение времени, в течение времени, за который сервер должен быть отсвея на каждом запросе

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

[New-AzStorageContainer](./New-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)


