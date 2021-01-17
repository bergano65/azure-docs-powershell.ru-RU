---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422743"
---
# Get-AzStorageTable

## SYNOPSIS
Список таблиц хранилища.

## СИНТАКСИС

### TableName (по умолчанию)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Get-AzStorageTable вы** можете перечислить таблицы хранилища, связанные с учетной записью хранения в Azure.

## ПРИМЕРЫ

### Пример 1. Список всех таблиц хранилища Azure
```
PS C:\>Get-AzStorageTable
```

Эта команда получает все таблицы хранилища для учетной записи хранения.

### Пример 2. Список таблиц хранилища Azure с использованием поддеревного знака
```
PS C:\>Get-AzStorageTable -Name table*
```

Для получения таблиц хранения, имена которых начинаются с таблицы, используются поддиавные знаки.

### Пример 3. Список таблиц хранилища Azure с использованием префикса имени таблицы
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Для получения таблиц *хранения,* имена которых начинаются с таблицы, используется параметр "Префикс".

## PARAMETERS

### -Контекст
Определяет контекст хранилища.
Для этого можно использовать New-AzStorageContext управления.

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
Указывает имя таблицы.
Если имя таблицы пустое, в этом списке будут перечислены все таблицы.
В противном случае будут перечислены все таблицы, которые соответствуют указанному имени или шаблону обычного имени.

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

### -Префикс
Указывает префикс, используемый в имени нужной таблицы или таблиц.
С помощью этой строки можно найти все таблицы, которые начинаются с одной и той же строки, например таблицы.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


