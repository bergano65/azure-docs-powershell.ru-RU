---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517106"
---
# Get-AzStorageQueue

## SYNOPSIS
Список очередей хранилища.

## СИНТАКСИС

### QueueName (по умолчанию)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для **этого с помощью cmdlet get-AzStorageQueue** перечислены очереди хранилища, связанные с учетной записью хранилища Azure.

## ПРИМЕРЫ

### Пример 1. Список всех очередей хранилища Azure
```
PS C:\>Get-AzStorageQueue
```

Эта команда возвращает список всех очередей хранилища для текущей учетной записи хранения.

### Пример 2. Список очередей хранилища Azure с использованием подстрок
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Эта команда использует подстройки для получения списка очередей хранилища, названия которых начинаются с очереди.

### Пример 3. Список очередей хранилища Azure с помощью префикса имени очереди
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

В этом примере параметр *Prefix* используется для получения списка очередей хранилища, имена которых начинаются с очереди.

## PARAMETERS

### -Контекст
Определяет контекст хранилища Azure.
Его можно создать с помощью **cmdlet New-AzStorageContext.**

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
Указывает имя.
Если имя не указано, получается список всех очередей.
Если задано полное или частичное имя, командлет получает все очереди, которые соответствуют шаблону имени.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Префикс
Указывает префикс, используемый в именах очередей, которые вы хотите получить.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
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

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


