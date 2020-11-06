---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566232"
---
# Get-AzureBatchNodeFileContent

## КРАТКИй обзор
Получает пакетный файл узла.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Task_Id_Path
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureBatchNodeFileContent** получает файл узла пакета Azure и сохраняет его в виде файла или потока.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение файла узла пакета, связанного с задачей, и сохранение файла
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла с именем StdOut.txt и сохраняет его в E:\PowerShell\StdOut.txt пути к файлу на локальном компьютере.
Файл узла StdOut.txt связан с задачей, которая имеет идентификатор Task01 для задания с ИД Job01.
Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.

### Пример 2: получение файла узла пакета и сохранение его по указанному пути с помощью конвейера
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла с именем StdErr.txt с помощью командлета Get-AzureBatchNodeFile.
Команда передает этот файл текущему командлету с помощью оператора конвейера.
Текущий командлет сохраняет этот файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.
Файл узла StdOut.txt связан с задачей, которая имеет идентификатор Task02 для задания с ИД Job02.

### Пример 3: получение файла узла пакета, связанного с задачей, и его направление в поток
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.

Вторая команда получает файл узла с именем StdOut.txt из задачи с ИД Task11 для задания с ИД Job03.
Команда направляет содержимое файла в поток в $Stream.

### Пример 4: получение файла узла на основе вычислительного узла и его сохранение
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла Startup\StdOut.txt из COMPUTE Node, который имеет ИД ComputeNode01 в пуле с ИД Pool01.
Команда сохраняет файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.

### Пример 5: получение файла узла на основе вычислительного узла и его сохранение с использованием конвейера
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Эта команда получает файл узла Startup\StdOut.txt с помощью Get-AzureBatchNodeFile из COMPUTE Node, у которого есть идентификатор ComputeNode01.
Вычислительный узел находится в пуле с ИДЕНТИФИКАТОРом Pool01.
Команда передает этот файл узла в текущий командлет.
Этот командлет сохраняет файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.

### Пример 6: получение файла узла из вычислительного узла и его направление в поток
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.

Вторая команда получает файл узла с именем StdOut.txt из COMPUTE Node, который имеет идентификатор ComputeNode01 в пуле с ИД Pool01.
Команда направляет содержимое файла в поток в $Stream.

## ПАРАМЕТРЫ

### -BatchContext
Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.
Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой. Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа. Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
Конец диапазона байтов для скачивания.
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
Начало диапазона байтов для загрузки.
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Указывает идентификатор вычислительного узла, содержащего файл узла, возвращаемый этим командлетом.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPath
Указывает путь к файлу, в котором командлет сохраняет файл узла.

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Указывает поток, в который этот командлет записывает содержимое файла узла.
Этот командлет не закрывает и не перематывает этот поток.

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Указывает файл, который получает этот командлет, как объект **PSNodeFile** .
Чтобы получить объект файла узла, используйте командлет Get-AzureBatchNodeFile.

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Указывает идентификатор задания, содержащего целевую задачу.

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Путь к файлу узла для скачивания.

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Указывает идентификатор пула, который содержит вычислительный узел, содержащий файл узла, который получает этот командлет.

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskId
Указывает идентификатор задачи.

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### BatchAccountContext
Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.

### PSNodeFile
Параметр "InputObject" принимает значение типа "PSNodeFile" из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)


