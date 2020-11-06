---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567180"
---
# Publish-AzureRmAutomationRunbook

## КРАТКИй обзор
Публикует Runbook.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Publish-AzureRmAutomationRunbook** публикует Runbook для использования в производственной среде службы автоматизации Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: публикация Runbook
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

Эта команда публикует Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации, в которой этот командлет публикует Runbook.

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

### -Name (имя)
Указывает имя Runbook, который публикует этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, для которой этот командлет публикует Runbook.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Automation. Model. Runbook

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Export-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[Get-AzureRmAutomationRunbook](./Get-AzureRMAutomationRunbook.md)

[Import-AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[New-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[New-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Remove-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)

[Start-AzureRmAutomationRunbook](./Start-AzureRMAutomationRunbook.md)


