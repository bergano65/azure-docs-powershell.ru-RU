---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 0302803568bac71baed28615552848f113da32df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731620"
---
# Get-AzAutomationDscOnboardingMetaconfig

## КРАТКИй обзор
Создает MOF-файлы с метаконфигурации.

## Максимальное

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzAutomationDscOnboardingMetaconfig** создает протоколы MOF-файлов, которые нужно использовать в МЕТАКОНФИГУРАЦИИ (DSC).
Этот командлет создает MOF-файл для каждого указываемого имени компьютера.
Командлет создает папку для файлов. mof.
Вы можете выполнить командлет Set-DscLocalConfigurationManager для этой папки, чтобы присоединить эти компьютеры к учетной записи службы автоматизации Azure как узлы DSC.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Встроенные серверы в автоматизацию DSC
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

Первая команда создает файлы мета-конфигурации DSC для двух серверов для учетной записи автоматизации с именем Contoso17.
Команда сохраняет эти файлы на рабочем столе.
Вторая команда использует командлет **Set-DscLocalConfigurationManager** , чтобы применить мета-конфигурацию к указанным компьютерам для их пошагового использования в качестве узлов DSC.

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации.
Вы можете выплата компьютеров, параметр *ComputerName* которых указывает на учетную запись, которую указывает этот параметр.

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

### -ComputerName
Указывает массив имен компьютеров, для которых этот командлет создает MOF-файлы.
Если этот параметр не указан, командлет создает MOF-файл для текущего компьютера (localhost).

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Force
Принудительное выполнение команды без запроса подтверждения и замена существующих MOF-файлов с одинаковыми именами.

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

### -OutputFolder
Указывает имя папки, в которой этот командлет хранит MOF-файлы.

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

### -ResourceGroupName
Указывает имя группы ресурсов.
Этот командлет создает файлы. mof на интегрированных компьютерах в группе ресурсов, которую указывает этот параметр.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### System. String []

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
