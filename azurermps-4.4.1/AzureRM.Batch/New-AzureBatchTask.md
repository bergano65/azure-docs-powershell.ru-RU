---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565653"
---
# New-AzureBatchTask

## КРАТКИй обзор
Создает пакетную задачу под заданием.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### JobId_Single (по умолчанию)
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobId_Bulk
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureBatchTask** создает пакетную задачу Azure в задании, указанной параметром *JOBID* , или параметром *задания* .

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание пакетной задачи
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

Эта команда создает задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИДЕНТИФИКАТОРом задания 000001.
Задача запускает указанную команду.
Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.

### Пример 2: создание пакетной задачи
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

Эта команда получает пакетное задание с ИД задания, 000001 с помощью командлета **Get-AzureBatchJob** .
Команда передает это задание текущему командлету с помощью оператора конвейера.
Команда создает задачу с ИДЕНТИФИКАТОРом Task26 под этим заданием.
Задача выполняет указанную команду с повышенными разрешениями.

### Пример 3: Добавление коллекции задач к указанному заданию с помощью конвейера
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.
Команда сохраняет ссылку на этот объект в переменной $Context.

Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.
Команды хранят задачи в $Task 01 и $Task 02.

Последняя команда получает пакетное задание с ИД задания 000001 с помощью **Get-AzureBatchJob**.
Затем команда передает это задание текущему командлету с помощью оператора конвейера.
Команда добавляет коллекцию задач под этим заданием.
Команда использует контекст, хранящийся в $Context.

### Пример 4: Добавление коллекции задач к указанному заданию
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.
Команда сохраняет ссылку на этот объект в переменной $Context.

Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.
Команды хранят задачи в $Task 01 и $Task 02.

Последняя команда добавляет задачи, которые хранятся в $Task 01 и $Task 02 под заданием с ИД задания 000001.

## ПАРАМЕТРЫ

### -AffinityInformation
Указывает подсказку о расположении, которую служба Batch использует для выбора узла, на котором необходимо выполнить задачу.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationPackageReferences
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BatchContext
Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.
Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.

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

### -CommandLine
Задает командную строку для задачи.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ограничения
Указывает ограничения на выполнение, которые применяются к этой задаче.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DependsOn
Указывает, что задача зависит от других задач.
Задача не будет планироваться до тех пор, пока все зависимые задачи не будут выполнены успешно.

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Указывает отображаемое имя задачи.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentSettings
Задает параметры среды в виде пар "ключ-значение", которые этот командлет добавляет к задаче.
Ключом является имя параметра среды.
Значение является параметром среды.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExitConditions
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор задачи.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Указывает задание, в рамках которого этот командлет создает задачу.
Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzureBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Указывает идентификатор задания, в рамках которого этот командлет создает задачу.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MultiInstanceSettings
Задает сведения о том, как выполнить задачу с несколькими экземплярами.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceFiles
Определяет файлы ресурсов в виде пар "ключ-значение", которые требуются для задачи.
Key — путь к файлу ресурсов.
Значением является источник больших двоичных объектов файла ресурсов.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunElevated
Указывает на то, что рабочий процесс запускается с правами администратора.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Задачи
Указывает коллекцию задач, которые нужно добавить.
Каждая задача должна иметь уникальный идентификатор.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### BatchAccountContext
Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.

### PSCloudJob
Параметр "задание" принимает значение типа "PSCloudJob" из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Get-AzureBatchTask](./Get-AzureBatchTask.md)

[New-AzureBatchTask](./New-AzureBatchTask.md)

[Remove-AzureBatchTask](./Remove-AzureBatchTask.md)

[Остановить-AzureBatchTask](./Stop-AzureBatchTask.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)


