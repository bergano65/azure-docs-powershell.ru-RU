---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 84b5389c4f9b404b4b74783184143af310bf1ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002323"
---
# New-AzStorageTable

## SYNOPSIS
Создает таблицу хранилища.

## СИНТАКСИС

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet New-AzStorageTable** создается таблица хранилища, связанная с учетной записью хранения в Azure.

## ПРИМЕРЫ

### Пример 1. Создание таблицы хранилища Azure
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

Эта команда создает таблицу хранилища с именем tableabc.

### Пример 2. Создание нескольких таблиц хранилища Azure
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

Эта команда создает несколько таблиц.
Для этого используется **метод разделения** класса .NET **String,** который передает имена в конвейере.

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
Указывает имя новой таблицы.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageTable](./Get-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


