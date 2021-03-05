---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013667"
---
# Export-AzDataLakeStoreChildItemProperty

## SYNOPSIS
Экспорт свойств (использование диска и ACL) для всего дерева из указанного пути на выходной путь.

## СИНТАКСИС

### GetDiskUsage
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetAllProperties
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetAclDump
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
**Export-AzDataLakeStoreChildItemProperty** используется для отчетов об использовании пространства ADLS или /и ACL для заданного каталога, а также о его подкадрах и файлах.

## ПРИМЕРЫ

### Пример 1. Использование дисков и ACL для всех поднаправлений и файлов
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

Получите данные об использовании диска и использовании ACL для всех поднаправлений и файлов в папке /a. IncludeFile гарантирует, что файл будет также включен в данные об использовании

### Пример 2. Использование ACL для всех поднаправлений и файлов с согласованным скрытым ACL
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

Получите использование ACL для всех поднаправленных библиотек и файлов в /a. IncludeFile гарантирует, что для файлов также будет фикс данных об использовании. HideconsistentAcl в этом случае будет показывать acl из /a, а не дети, так как у всех детей то же самое, что и /a. Этот флаг пропускает выход из подпотока, если все это acls, то же самое, что и корневой.

## PARAMETERS

### -Account
Учетная запись Data Lake Store для выполнения операции filesystem в

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Concurrency
Количество обработанных параллельно файлов и каталогов.
Значение по умолчанию будет вычисляться как наилучшее решение на основе спецификации системы.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -GetAcl
Извлекает acl, начиная с корневого пути.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GetDiskUsage
Извлекает использование диска, начиная с корневого пути.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HideConsistentAcl
Не показывать подпоток каталога, если ALS одинаковы во всем подпотоке. Это упрощает просмотр только путей, до которых отличаются ALS. Например, если все файлы и папки в /a/b одинаковы, не отобразить поддерев /a/b, а просто вычесть /a/b со "True" в столбце "Согласованная ACLCannot", если includeFiles не задавается, так как не удалось определить согласованную папку ACL без иска для файлов.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFile
Статистика на уровне файлов (по умолчанию — только сведения на уровне каталога)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaximumDepth
Максимальная глубина от корневого каталога до отображения использования диска или acl

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputPath
Путь к выходной файлу. Может быть локальным или Adl-путем. По умолчанию он локальный. Если задан путь SaveToAdl, это путь ADL в той же учетной записи

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Путь в указанной учетной записи Data Lake, который нужно извлечь.
Может быть файлом или папкой в формате '/folder/file.txt', где первая после DNS "/" указывает корневую папку файловой системы.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveToAdl
Если он прошел, файл дампов сохраняется в ADL.
В этом случае ДампФайл будет путем ADL

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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

### System.String

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance

### System.Management.Automation.SwitchParameter

### System.Int32

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
