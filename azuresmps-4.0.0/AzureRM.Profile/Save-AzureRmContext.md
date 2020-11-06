---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554916"
---
# Save-AzureRmContext

## КРАТКИй обзор
Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.

## Максимальное

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## NОПИСАНИЕ
Командлет Save-AzureRmContext сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Сохранение контекста текущего сеанса
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

В этом примере контекст Azure текущего сеанса сохраняется в указанном JSON-файле.

### Пример 2: сохранение определенного контекста
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

В этом примере выполняется сохранение контекста Azure, который передается в командлет, в указанный JSON файл.

## ПАРАМЕТРЫ

### -Force
Перезаписать заданный файл, если он существует

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Задает путь к файлу, в который нужно сохранить сведения для проверки подлинности.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает контекст Azure, из которого считывается этот командлет.
Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Profile. Models. PSAzureProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

