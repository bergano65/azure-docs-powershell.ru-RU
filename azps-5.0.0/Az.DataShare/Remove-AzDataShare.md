---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312923"
---
# Remove-AzDataShare

## КРАТКИй обзор
Удаление общего доступа к данным.

## Максимальное

### ByFieldsParameterSet (по умолчанию)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzDataShare** удаляет общий доступ к данным.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Эта команда удаляет из учетной записи общего доступа к данным Azure общий доступ к данным с именем AdsShare из WikiAds. 

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Имя учетной записи для общего доступа к данным Azure

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob описание}}

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект общего доступа к данным Azure "" YAML: PSDataShare наборы параметров: ByObjectParameterSet псевдонимы: 

Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByValue) сохранить подстановочные знаки: ложь

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Имя общего доступа к данным Azure

Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы: 

Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращаемый объект (если указан).

Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: 

Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false

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

### -ResourceGroupName
Имя группы ресурсов для учетной записи общего доступа к данным Azure

Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы: 

Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса общего ресурса данных Azure

Тип YAML: наборы строковых параметров: ByResourceIdParameterSet псевдонимы: 

Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByPropertyName) сохранить подстановочные знаки: ложь

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: CF

Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: Wi

Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false




Тип YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare наборы параметров: ByObjectParameterSet псевдонимы:

Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByValue) сохранить подстановочные знаки: ложь

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
