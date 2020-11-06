---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570000"
---
# New-AzureBatchJob

## КРАТКИй обзор
Создание задания в пакетной службе.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureBatchJob** создает задание в пакетной службе Azure в учетной записи, указанной в параметре *BatchAccountContext* .

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание задания
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

Первая команда создает объект **PSPoolInformation** с помощью командлета New-Object.
Команда сохраняет этот объект в переменной $PoolInformation.

Вторая команда присваивает идентификатор Pool22 свойству **PoolId** объекта в $PoolInformation.

Последняя команда создает задание с ИДЕНТИФИКАТОРом ContosoJob35.
Задачи, добавленные в задание, выполняются в пуле с ИД Pool22.
Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.

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

### -CommonEnvironmentSettings
Задает общие переменные среды, такие как пары "ключ-значение", которые устанавливаются этим командлетом для всех задач в задании.
Ключом является имя переменной среды.
Значением является значение переменной среды.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ограничения
Указывает ограничения на выполнение для задания.

```yaml
Type: PSJobConstraints
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Указывает отображаемое имя задания.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор задания.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobManagerTask
Указывает задачу диспетчера задач.
Пакетная служба запускает задачу "Диспетчер задач" при запуске задания.

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobPreparationTask
Указывает задачу подготовки задания.
Пакетная служба запускает задачу подготовки задания на вычислительном узле, прежде чем она начнет выполнение каких-либо задач этого задания на этом вычислительном узле.

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobReleaseTask
Указывает задачу выпуска задания.
Пакетная служба запускает задачу задания выпуска, когда задание завершается.
Пакетная служба запускает задачу выпуска задания на каждом из узлов вычислительной сети, в которых выполнялась какая-либо задача задания.

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
Задает метаданные в виде пар "ключ-значение", которые нужно добавить в задание.
Ключом является имя метаданных.
Значением является значение метаданных.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnAllTasksComplete
Указывает действие, выполняемое пакетной службой, если все задачи в задании находятся в завершенном состоянии.

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnTaskFailure
Указывает действие, выполняемое пакетной службой в случае сбоя какой – либо задачи в задании.

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolInformation
Задает сведения о пуле, в котором Пакетная служба выполняет задачи задания.

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority (приоритет)
Задает приоритет задания.
Допустимые значения: целые числа от-1000 до 1000.
Значение-1000 является самым низким приоритетом.
Значение 1000 — самый высокий приоритет.
Значение по умолчанию — 0.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsesTaskDependencies
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

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

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureBatchJob](./Disable-AzureBatchJob.md)

[Enable-AzureBatchJob](./Enable-AzureBatchJob.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[Remove-AzureBatchJob](./Remove-AzureBatchJob.md)

[Остановить-AzureBatchJob](./Stop-AzureBatchJob.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)


