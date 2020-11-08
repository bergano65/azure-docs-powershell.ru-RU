---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249359"
---
# Get-AzDataLakeGen2ChildItem

## КРАТКИй обзор
Перечисление подкаталогов и файлов из корневой папки или из корня файловой системы.

## Максимальное

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzDataLakeGen2ChildItem** включает в себя подкаталоги и файлы в каталоге или файловой системе учетной записи хранения Azure.
Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен. Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список прямых вложенных элементов из файловой системы
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

Эта команда перечисляет прямые подразделы в файловой системе.

### Пример 2: рекурсивный список из каталога и выбор свойств и ACL
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

Эта команда перечисляет прямые подразделы в файловой системе.

### Пример 3: рекурсивное перечисление элементов из файловой системы в нескольких пакетах
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

В этом примере параметры *maxcount* и *ContinuationToken* используются для рекурсивного перечисления элементов из файловой системы в нескольких пакетах.
Первые четыре команды назначают значения переменным для использования в примере.
Пятая команда задает оператор **Do-** in, использующий командлет **Get-AzDataLakeGen2ChildItem** для элементов списка.
Оператор включает токен продолжения, хранящийся в переменной $Token.
$Token изменения значения по мере выполнения цикла.
В последней команде используется команда **echo** для отображения итогового значения.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме

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

### -Context
Объект контекста хранилища Azure

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
Маркер продолжения.

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

### -FetchProperty
Получение свойств и списка ACL для DataItem.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem
Имя файловой системы

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Максимальное количество больших двоичных объектов, которые могут быть возвращены.

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

### -OutputUserPrincipalName
Если speicify этот параметр, значения идентификаторов пользователей, возвращаемые в полях владелец и группа каждого элемента списка, будут преобразованы из идентификаторов объектов Azure Active Directory в имена участников-пользователей. Если этот параметр не speicify, значения будут возвращены как идентификаторы объектов Azure Active Directory. Обратите внимание, что идентификаторы объектов Group и Application не переводятся, так как они не имеют уникальных понятных имен.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Путь в указанной файловой системе, который нужно извлечь.
Должен быть каталогом в формате "Directory1/Directory2/".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Рекурсия
Указывает, будет ли рекурсивно получен дочерний элемент.
По умолчанию используется значение false.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
