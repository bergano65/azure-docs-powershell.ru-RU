---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563692"
---
# New-AzureVMSqlServerAutoPatchingConfig

## КРАТКИй обзор
Создает объект конфигурации для автоматического исправления на виртуальной машине.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureVMSqlServerAutoPatchingConfig** создает объект конфигурации для автоматического исправления на виртуальной машине.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта конфигурации для настройки автоматического исправления
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Эта команда создает объект конфигурации для исправления.
Команда задает день недели и определяет окно обслуживания.
Эта конфигурация включает исправление, использующее эти значения.
Команда сохраняет результат в переменной $AutoBackupConfig.
Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzureRmVMSqlServerExtension.

## ПАРАМЕТРЫ

### -DayOfWeek
Указывает день недели, когда необходимо установить обновления.

Для этого параметра допустимы следующие значения:

- Воскресеньям
- Вторник
- Вторник
- Четверг
- Вторник
- Пт
- Субботам
- Жизни

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable (включить)
Указывает на то, что автоматическая установка исправлений для виртуальной машины включена.
Если вы включите автоматическое исправление, командлет поместит обновление Windows в интерактивный режим.
Если отключить автоматическое исправление, параметры центра обновления Windows не изменяются.

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

### -MaintenanceWindowDuration
Указывает продолжительность (в минутах) периода обслуживания.
Автоматическое исправление устраняет выполнение действия, которое может повлиять на доступность виртуальной машины за пределами этого окна.
Укажите кратное 30 минут.

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

### -MaintenanceWindowStartingHour
Указывает час дня, когда запускается окно обслуживания.
Это время определяет время начала установки обновлений.

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

### -PatchCategory
Указывает, следует ли включать важные обновления.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

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
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### AutoPatchingSettings
Этот командлет возвращает объект, содержащий параметры автоматического исправления.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


