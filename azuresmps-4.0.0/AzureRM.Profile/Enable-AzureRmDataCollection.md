---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555640"
---
# Enable-AzureRmDataCollection

## КРАТКИй обзор
Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов AzurePowerShell.
Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.
Никакие данные не собираются, пока не будет явно задействовано.

## Максимальное

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.
Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzureRmDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.
Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.
Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.

Запустите командлет Enable-AzureRMDataCollection, чтобы включить сбор данных для текущего пользователя на этом компьютере.
Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.

Чтобы отключить сбор данных для текущего пользователя, выполните командлет Disable-AzureRmDataCollection.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Включение сбора данных для текущего пользователя
```
PS C:\> Enable-AzureRmDataCollection
```

В этом примере показано, как включить сбор данных для текущего пользователя.

## ПАРАМЕТРЫ

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Ничего

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureRmDataCollection]()

