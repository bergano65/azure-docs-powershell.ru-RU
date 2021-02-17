---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239333"
---
# Get-AzBatchNodeFileContent

## SYNOPSIS
Получает пакетный файл узла.

## СИНТАКСИС

### Task_Id_Path
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Get-AzBatchNodeFileContent** получает пакетный файл узла Azure и сохраняет его как файл или поток.

## ПРИМЕРЫ

### Пример 1. Получите пакетный файл узла, связанный с задачей, и сохраните его
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла с именем StdOut.txt и сохраняет его в E:\PowerShell\StdOut.txt пути на локальном компьютере.
Файл StdOut.txt связан с задачей, которая имеет задачу "ID Task01" для задания, которое имеет задание "ИД01".
Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.

### Пример 2. Получите пакетный файл узла и сохраните его в заданный путь к файлу с помощью конвейера.
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла с именем "StdErr.txt с помощью Get-AzBatchNodeFile командлета.
Эта команда передает этот файл текущему командлету с помощью оператора конвейера.
Текущий cmdlet сохраняет этот файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.
Файл StdOut.txt связан с задачей, которая имеет задачу "ID Task02" для задания, которое имеет задание "ИД02".

### Пример 3. Получить пакетный файл узла, связанный с задачей, и направить его в поток
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Первая команда создает поток с помощью New-Object командлета, а затем сохраняет его в $Stream переменной.
Вторая команда получает файл узла, который называется StdOut.txt из задачи, которая имеет задачу "ИД11" для задания, для которого назначено задание "ИД03".
Команда направляет содержимое файла в поток в $Stream.

### Пример 4. Получите файл узла из узла вычислений и сохраните его
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла Startup\StdOut.txt узла вычислений, который содержит ID ComputeNode01 в пуле, который содержит пул ID Pool01.
Команда сохраняет файл в папкуE:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.

### Пример 5. Получите файл узла из узла вычислений и сохраните его с помощью конвейера
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла Startup\StdOut.txt с помощью Get-AzBatchNodeFile узла вычислений, который имеет ID ComputeNode01.
Узел вычислений находится в пуле с пулом ID Pool01.
Эта команда передает этот файл узла текущему командлету.
Он сохраняет файл в папку, E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.

### Пример 6. Получить файл узла из узла вычислений и направить его в поток
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Первая команда создает поток с помощью New-Object командлета, а затем сохраняет его в $Stream переменной.
Вторая команда получает файл узла с именем StdOut.txt из узла вычислений, в пуле которого есть ID ComputeNode01.
Команда направляет содержимое файла в поток в $Stream.

## PARAMETERS

### -BatchContext
Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.
Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory. Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию. Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
Конец загружаемого диапазона byte.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
Начало загружаемого диапазона byte.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Определяет код узла вычислений, содержаного файл узла, который возвращает этот cmdlet.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
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

### -DestinationPath
Путь к файлу, в котором этот cmdlet сохраняет файл узла.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Определяет поток, в который этот cmdlet записывает содержимое файла узла.
Этот cmdlet не закрывает и не перемотать этот поток.

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Определяет файл, который получает этот cmdlet как **объект PSNodeFile.**
Чтобы получить объект в файле узла, используйте Get-AzBatchNodeFile-файл.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Определяет ИД задания, которое содержит целевую задачу.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Путь к файлу узла, который нужно скачать.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Определяет код пула, который содержит узел вычислений, содержащий файл узла, который получает этот cmdlet.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskId
Определяет ИД задачи.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSNodeFile

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchNodeFile](./Get-AzBatchNodeFile.md)

[Пакетные cmdlets Azure](/powershell/module/Az.Batch/)
