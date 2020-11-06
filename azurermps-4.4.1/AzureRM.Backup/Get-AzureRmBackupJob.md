---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559947"
---
# Get-AzureRmBackupJob

## КРАТКИй обзор
Получает задания резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### "Фильтры" (по умолчанию)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBackupJob** получает задания резервного копирования Azure для определенного хранилища.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех заданий в резервном хранилище
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .
Команда сохраняет этот объект в переменной $Vault.

Вторая команда получает все задания для хранилища в $Vault.

### Пример 2: Получение завершенных заданий
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Эта команда получает завершенные задания из хранилища в $Vault.

### Пример 3: получение заданий со сбоем за последнюю неделю
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Эта команда возвращает задания с ошибкой за последнюю неделю из хранилища в $Vault.
Параметр *from* указывает время в прошлом на семь дней.
В команде не указывается значение параметра " *Кому* ".
Таким образом, используется значение по умолчанию для текущего времени.

### Пример 4: создание резервной копии для выполняемого задания, которое завершается
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.

В первой строке сценария возвращаются все задания в $Vault, которые находятся в процессе выполнения, а затем эти задания сохраняются в переменной массива $Jobs.

Вторая строка сохраняет первое задание из массива $Jobs в переменной $Job.

Третья строка начинается с цикла **while** , который проверяет текущее состояние задания до завершения задания.
Чтобы получить сведения о ключевом слове " **время** ", введите `Get-Help about_While` .

Цикл **while** записывает на консоль сообщение, заждет десять секунд, а затем обновляет переменную $Job.
Сценарий обновляет переменную $Job с помощью существующего значения $Job и текущего командлета, чтобы получить текущее состояние задания.
Чтобы получить сведения о командлетах Windows PowerShell, введите `Get-Help Write-Host` и `Get-Help Start-Sleep` .

В последней строке сценария сообщается, что сценарий завершен.

## ПАРАМЕТРЫ

### -From
Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.
Чтобы получить объект **DateTime** , используйте командлет Get-Date.
Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Указывает задание, которое получает этот командлет.
Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Указывает идентификатор задания, которое получает этот командлет.
Идентификатор — это свойство **InstanceId** объекта **AzureRmBackupJob** .
Чтобы получить объект **AzureRmBackupJob** , используйте Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Эксплуатация
Указывает операцию заданий, которые получает этот командлет.
Для этого параметра допустимы следующие значения:

- Копирование 
- ConfigureBackup 
- DeleteBackupData 
- Отменить 
- Восстановление 
- Снять защиту 
- Отмените регистрацию

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status (состояние)
Указывает состояние заданий, которые получает этот командлет.
Для этого параметра допустимы следующие значения:

- Ход выполнения
- Ошибкой
- Отменен
- Отмена
- Completed
- CompletedWithWarnings 

Вы можете указать этот параметр, чтобы найти все выполняемые задания или все задания, для которых произошел сбой.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.
Значение по умолчанию — текущее системное время.
Если указать этот параметр, необходимо также указать параметр *from* .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (тип)
Указывает тип контейнера, для которого этот командлет получает задания резервного копирования.
В настоящее время единственным поддерживаемым значением является значение AzureVM.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище резервных копий, для которого этот командлет получает задания.
Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRmBackupVault

## НАПРЯЖЕНИЕ

### AzureRmBackupJob[]
Этот командлет возвращает одно или несколько заданий резервного копирования.

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Остановить-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


