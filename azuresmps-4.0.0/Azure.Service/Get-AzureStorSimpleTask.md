---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075552"
---
# Get-AzureStorSimpleTask

## КРАТКИй обзор
Возвращает состояние задачи на устройстве StorSimple.

## Максимальное

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorSimpleTask** получает состояние задачи, которая выполняется асинхронно на устройстве Azure StorSimple.

При управлении устройством StorSimple большинство операций создания, чтения, обновления и удаления могут выполняться асинхронно.
Windows PowerShell возвращает элемент **taskId**.
Используйте идентификатор, чтобы получить текущее состояние задачи.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение состояния задачи
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Эта команда возвращает состояние задачи с указанным ИДЕНТИФИКАТОРом.
Результат показывает, что задача имеет состояние завершено и является результатом успеха.

## ПАРАМЕТРЫ

### -InstanceId
Указывает идентификатор задачи, для которой этот командлет отслеживает состояние.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### JobStatusInfo
Этот командлет возвращает объект **TaskStatusInfo** , который включает следующие поля: 

- **Ошибка**.
**ErrorDetails** , который включает **код** и **сообщение**.
- **TaskId**.
**String**.
Идентификатор задачи, для которой возвращается состояние.
- **TaskSteps**.
**IList \<TaskStep\>**.
Каждый объект **TaskStep** имеет **подробные данные** , **ErrorCode** , **сообщение** , **результат** и **состояние**.
- **Результат**.
**TaskResult** , который включает общие результаты задачи.
Допустимые значения: ошибка, успешно, PartialSuccess, отменено и недопустимо.
- **Состояние**.
**TaskStatus** , который включает общее состояние выполнения задачи.
Допустимые значения: "выполняется, недопустимо" и "завершено".
- **TaskResult**.
**TaskResult** — значение, вычисленное на основе **результата** и **состояния**.
Допустимые значения: ошибка, успешно, PartialSuccess, отмена и недопустимый.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

