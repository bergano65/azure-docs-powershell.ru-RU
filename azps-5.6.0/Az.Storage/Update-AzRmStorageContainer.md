---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 696070e19f1810ab352abde4ad6248f4bf42b180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973320"
---
# Update-AzRmStorageContainer

## SYNOPSIS
Модификатор контейнера BLOB-хранилищ

## СИНТАКСИС

### AccountName (по умолчанию)
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContainerObject
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Update-AzRmStorageContainer** изменяет контейнер BLOB-хранилищ.

## ПРИМЕРЫ

### Пример 1. Изменяет метаданные и общедоступный доступ для контейнера BLOB-хранилищ с помощью имени учетной записи и имени контейнера хранилища.
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

Эта команда изменяет метаданные контейнера BLOB-хранилищ и общедоступный доступ с именем учетной записи хранения и именем контейнера.

### Пример 2. Отключение общего доступа для контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

Эта команда отключает общедоступный доступ к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.

### Пример 3. Настройка общего доступа в качестве BLOB-проектов для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

Эта команда настроит общедоступный доступ в качестве BLOB-проектов для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект контейнера хранилища

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Метаданные
Метаданные контейнера

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя контейнера

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PublicAccess
Container PublicAccess

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
Объект учетной записи хранения

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Имя учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

### Microsoft.Azure.Commands.Management.Storage.Models.PSContainer

## OUTPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSContainer

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
