---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001736"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Создает объект конфигурации для автоматического исправления на виртуальной машине.

## СИНТАКСИС

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для автоматического исправления на виртуальной машине создается объект конфигурации **new-AzVMSqlServerAutoPatchingConfig.**

## ПРИМЕРЫ

### Пример 1. Создание объекта конфигурации для настройки автоматического исправления
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Эта команда создает объект конфигурации для исправления.
Команда определяет день недели и окно обслуживания.
Эта конфигурация позволяет исправления, использующие эти значения.
Команда сохраняет результат в переменной $AutoBackupConfig.
Вы можете указать этот элемент конфигурации для других Set-AzVMSqlServerExtension.

## PARAMETERS

### -DayOfWeek
Определяет день недели, когда должны быть установлены обновления.
Допустимыми значениями для этого параметра являются:
- Воскресенье
- Понедельник
- Вторник
- Среда
- Четверг
- Пятница
- Суббота
- Каждый день

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Означает, что включено автоматическое исправление для виртуальной машины.
Если включить автоматическое исправление, с помощью cmdlet вы сможете переналиться в интерактивный режим Windows.
Если отключить автоматическое исправление, параметры Обновления Windows не изменятся.

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

### -MaintenanceWindowDuration
Длительность (в минутах) окна обслуживания.
Автоматическое исправление позволяет избежать выполнения действий, которые могут повлиять на доступность виртуальной машины за пределами этого окна.
Укажите кратное 30 минут.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
Определяет час, в который день начинается окно обслуживания.
Это время определяет, когда начнется установка обновлений.

```yaml
Type: System.Int32
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
Type: System.String
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


