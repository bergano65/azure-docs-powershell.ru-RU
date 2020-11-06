---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558552"
---
# New-AzureRmBackupRetentionPolicyObject

## КРАТКИй обзор
Создание политики хранения резервных копий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmBackupRetentionPolicyObject** создает политику хранения резервных копий Azure.
Политика хранения определяет, как долго резервная копия будет хранить точку восстановления.
Типы хранения описаны ниже. 
- За 
- Запуск 
- Исходящем 
- Ежегодно создайте одну политику хранения для каждого типа хранения, который вы планируете использовать.
Политика резервного копирования связана по крайней мере с одной политикой хранения.
Чтобы создать политику архивации, используйте командлет New-AzureRmBackupProtectionPolicy.
Вместо этого вы можете предоставить политику хранения для командлета Enable-AzureRmBackupProtection.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание политики хранения для ежедневной сохранности
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

Первая команда создает политику хранения в течение 30 дней ежедневной сохранности, а затем сохраняет ее в переменной $Daily.
Вторая команда отображает содержимое $Daily.

### Пример 2: создание ежемесячной политики хранения
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

В первой команде создается политика хранения, которая хранит резервные копии на десятой и двадцатой части каждого месяца в течение двенадцати месяцев.
Эта команда сохраняет политику хранения в переменной $Monthly.
Вторая команда отображает содержимое $Monthly.

## ПАРАМЕТРЫ

### -DailyRetention
Указывает на то, что этот командлет создает ежедневный параметр политики хранения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
Задает дни месяца, которые определяют, какие из резервных точек восстановления хранятся и как долго.
Допустимые значения этого параметра: целые числа от 1 до 28 и последний.
Укажите этот параметр, если указаны параметры *DailyRetention* , *MonthlyRetentionInDailyFormat* и *YearlyRetentionInDailyFormat* .

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases:
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Указывает массив дней недели.
Дни, указанные этим командлетом, определяют, какие точки восстановления хранятся в резервной копии и как долго.
Для этого параметра допустимы следующие значения:
- Вторник 
- Вторник 
- Четверг 
- Вторник 
- Пт 
- Субботам 
- Воскресенье. Этот параметр указывается, если указаны параметры *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* и *YearlyRetentionInWeeklyFormat* .
Убедитесь в том, что дни недели, которые вы выбрали для резервного копирования и для хранения, выровнены.
Например, если для резервной копии задано значение "Суббота", политики хранения должны также использовать субботу.

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -MonthlyRetentionInDailyFormat
Указывает на то, что этот командлет создает месячную политику в ежедневном формате.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
Указывает на то, что этот командлет создает месячную политику в еженедельном формате.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
Указывает, в каких месяцах года должны быть точки восстановления, которые будут храниться в течение ежегодной базы данных.
Допустимые значения этого параметра: названия месяцев, например Январь или февраль.

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранение
Указывает срок хранения (в днях, месяцах или годах), для которого резервная копия хранит резервную точку.
Единица зависит от того, выбрал ли этот командлет ежедневные, ежемесячные или ежегодные параметры хранения.
Например, если указать параметр *DailyRetention* , командлет интерпретирует текущий параметр как количество дней.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklyRetention
Указывает на то, что этот командлет создает еженедельную политику хранения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekNumber
Указывает недели месяца, которые определяют, какие из резервных точек восстановления хранятся и как долго.
Для этого параметра допустимы следующие значения:
- Первич 
- 2 
- Третьего 
- Заканчива 
- Времени

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
Указывает на то, что этот командлет создает политику хранения ежегодно в ежедневном формате.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
Указывает на то, что этот командлет создает политику хранения ежегодно в недельном формате.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
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

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRetentionPolicy

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[New-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


