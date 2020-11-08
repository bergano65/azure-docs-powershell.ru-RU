---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076467"
---
# Remove-AzureStorSimpleDeviceBackup

## КРАТКИй обзор
Удаляет объект резервного копирования.

## Максимальное

### IdentifyById (по умолчанию)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureStorSimpleDeviceBackup** удаляет один объект резервного копирования.
При попытке удалить резервную копию, которая уже удалена, этот командлет возвращает ошибку.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление резервной копии для устройства
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Эта команда удаляет резервную копию с указанным ИДЕНТИФИКАТОРом для устройства с именем Contoso63-AppVm.
Команда запускает операцию, которая удаляет объект **резервного копирования** , а затем возвращает объект **TaskResponse** .
Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .

### Пример 2: удаление первой резервной копии устройства с помощью идентификатора
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

Первая команда получает резервные копии для устройства с именем Contoso63-AppVm, а затем сохраняет их в переменной $Backup.

Вторая команда удаляет резервную копию с устройства с именем Contoso63-AppVm.
В команде используется стандартная точечная нотация для ссылки на свойство **InstanceId** первого элемента массива $Backup.
Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .

### Пример 3: удаление первой резервной копии устройства с помощью конвейера
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

Первая команда получает резервные копии для устройства с именем Contoso63-AppVm, а затем сохраняет их в переменной $Backup.

Вторая команда передает первый объект, хранящийся в массиве $Backup, в текущий командлет.
Этот командлет удаляет эту резервную копию с устройства с именем Contoso63-AppVm.
Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .

## ПАРАМЕТРЫ

### -Резервное копирование
Указывает удаляемый объект **резервного копирования** .
Чтобы получить объект **резервного копирования** , используйте командлет **Get-AzureStorSimpleDeviceBackup** .

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupId
Задает ИД экземпляра удаляемого архива.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Имя_устройства
Указывает имя устройства StorSimple, на котором нужно удалить резервную копию.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Указывает на то, что этот командлет не запрашивает подтверждение.

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

### -Profile
Указывает профиль Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.

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

### Копирование

## НАПРЯЖЕНИЕ

### TaskStatusInfo, TaskResponse
Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* если этот параметр не указан, функция возвращает объект **TaskResponse** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


