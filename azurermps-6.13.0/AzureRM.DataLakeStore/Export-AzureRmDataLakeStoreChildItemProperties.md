---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
ms.openlocfilehash: faaf8a0c614a1243a3e3812cd0b6e1202cc7e75b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566488"
---
# Export-AzureRmDataLakeStoreChildItemProperties

## КРАТКИй обзор
Экспорт свойств (использование дискового пространства и ACL) для всего дерева по заданному пути на OUPUT путь.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### GetDiskUsage
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetAllProperties
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetAclDump
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
**Export-AzureRmDataLakeStoreChildItemProperties** используется для составления отчета об использовании пространства ADLS или об использовании ACL для определенного каталога, а также его вложенных папок и файлов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: использование дискового пространства и использование ACL для всех подкаталогов и файлов
```
PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

Получение сведений об использовании диска и использовании ACL для всех подкаталогов и файлов в разделе/a. IncludeFile обеспечивает получение сведений о том, что они также будут использоваться для файлов

### Пример 2: получение сведений об использовании ACL для всех подкаталогов и файлов с скрытым списком ACL
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzureRmDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

Получение сведений об использовании ACL для всех подкаталогов и файлов в разделе/a. IncludeFile гарантирует получение сведений о том, что они будут использоваться для файлов. HideconsistentAcl в этом случае будет показывать ACL для/a, а не дети, так как все дочерние элементы имеют тот же список ACL, что и/a. Этот флаг пропускает OUPUT ACL для поддерева, если все его ACL совпадают с корнем.

## ПАРАМЕТРЫ

### -Account (учетная запись)
Учетная запись Data Lake Store для выполнения операции файловой системы

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

### -Параллелизм
Указывает количество параллельных файлов или каталогов.
Значение по умолчанию будет вычислено для наилучшего усилия на основе спецификации системы.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GetAcl
Извлекает список ACL, начиная с корневого пути.

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
Не показывать поддерево каталогов, если все списки ACL одинаковы во всем поддереве. Это упрощает просмотр только тех путей, до которых они отличаются. Например, если все файлы и папки в/a/b совпадают, не выполняйте subtreeunder/a/b и просто выводите значение "истина" в списке "", если параметр ColumnCannot не установлен, так как не удается определить список ACL, не получая списки ACL для файлов.

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
Отображать статистику на уровне файлов (по умолчанию отображаются только сведения на уровне каталога)

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
Максимальная глубина в корневом каталоге, в которой отображаются сведения об использовании диска и ACL

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
Путь к выходному файлу. Это может быть локальный путь или ADL путь. По умолчанию он является локальным. Если SaveToAdl — pecified, то это путь к ADL в той же учетной записи

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
Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.

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
Путь в заданной учетной записи Data Lake, которую необходимо получить.
Может быть файлом или папкой в формате "/Folder/file.txt", где первый символ "/" после DNS указывает на корневой каталог файловой системы.

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
После перепередачи файл дампа сохраняется в ADL.
Будет DumpFile в этом случае — это путь к ADL

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### System. Management. Automation. SwitchParameter

### System. Int32

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
