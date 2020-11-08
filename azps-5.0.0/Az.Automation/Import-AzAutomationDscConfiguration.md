---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: dbf33873f900b02888223a281a8050bdbe9b74d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247852"
---
# Import-AzAutomationDscConfiguration

## КРАТКИй обзор
Импортирует конфигурацию DSC в автоматизацию.

## Максимальное

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Import-AzAutomationDscConfiguration** импортирует конфигурацию необходимой конфигурации (DSC) ТД в Azure Automation.
Укажите путь к сценарию AP, содержащему единственную конфигурацию DSC.

## ИЛЛЮСТРИРУЮТ

### Пример 1: импорт конфигурации DSC в автоматизацию
```powershell
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

Эта команда импортирует конфигурацию DSC в файле с именем client.ps1 в учетную запись автоматизации с именем Contoso17. Команда задает параметр *Force* . Если у вас уже есть конфигурация DSC, эта команда заменяет ее.

### Пример 2

Импортирует конфигурацию DSC в автоматизацию. (автоматически сформированные)

<!-- Aladdin Generated Example -->
```powershell
Import-AzAutomationDscConfiguration -AutomationAccountName 'Contoso17' -Published -ResourceGroupName 'ResourceGroup01' -SourcePath 'C:\DSC\client.ps1'
```

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации, на которую этот командлет импортирует конфигурацию DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Описание
Задает описание конфигурации, импортируемой этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Указывает на то, что этот командлет заменяет существующую конфигурацию DSC в автоматизации.

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

### -LogVerbose
Указывает, включает ли этот командлет подробный вход и отключение для заданий компиляции данной конфигурации DSC. Укажите значение $True, чтобы включить или отключить подробный вход, и $False, чтобы отключить его.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Опубликовано
Указывает на то, что этот командлет импортирует конфигурацию DSC в опубликованном состоянии.

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
Указывает имя группы ресурсов, для которой этот командлет импортирует конфигурацию DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Источник
Указывает путь wps_2 сценария, содержащего конфигурацию DSC, которую этот командлет импортирует.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Теги
Пары "ключ-значение" в виде хэш-таблицы. Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### System. Collections. IDictionary

### System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Command. Automation. Model. DscConfiguration

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Export-AzAutomationDscConfiguration](./Export-AzAutomationDscConfiguration.md)

[Get-AzAutomationDscConfiguration](./Get-AzAutomationDscConfiguration.md)
