---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 46fff0df9eddc417f823aa7b0243824befb974e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973283"
---
# Update-AzStorageBlobServiceProperty

## SYNOPSIS
Изменяет свойства службы для службы BLOB-объектов хранилища Azure.

## СИНТАКСИС

### AccountName (по умолчанию)
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BlobServicePropertiesResourceId
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Update-AzStorageBlobServiceProperty** изменяет свойства службы для службы BLOB-объектов хранилища Azure.

## ПРИМЕРЫ

### Пример 1. Настройка службы BLOB-2018 DefaultServiceVersion для 2018-03-28
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

Эта команда задает для службы Blob Service DefaultServiceVersion значение 2018-03-28.

### Пример 2. Enable Changefeed в службе BLOB-хранилищ учетной записи хранения
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

Эта команда позволяет использовать changefeed в службе BLOB-устройств службы поддержки веб-канала изменения учетной записи хранения в хранилище BLOB-устройств Azure, прослушивая учетную запись хранилища GPv2 или BLOB-хранилищ для всех событий создания, изменения или удаления BLOB-хранилищ. Затем он выводит упорядоченный журнал событий для BLOB-$blobchangefeed в учетной записи хранения. Последовательные изменения сохраняются в файле Apache Avro и обрабатываются асинхронно и пошагово.

### Пример 3. Enable Versioning on Versioning on Blob service of a Storage account
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

Эта команда позволяет использовать службу BLOB-данных учетной записи хранения.

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

### -DefaultServiceVersion
Версия службы по умолчанию для настройки

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableChangeFeed
Включите ведение журнала изменения веб-канала для учетной записи хранения, заключив $true, отключите его, заключив для $false.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsVersioningEnabled
Если установлено это в этом случае, включено или настроено переключение версий.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Ввести ИД ресурса учетной записи хранения или свойства ресурса службы BLOB-объектов.

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
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
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Имя учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
