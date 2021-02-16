---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235292"
---
# Get-AzAutomationConnection

## SYNOPSIS
Подключение автоматизации.

## СИНТАКСИС

### ByAll (по умолчанию)
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConnectionName
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConnectionTypeName
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для **этого требуется одно или** несколько подключений автоматизации Azure.
По умолчанию этот cmdlet извлекает все подключения.
Укажите имя подключения, чтобы получить определенное подключение.
Укажите имя типа подключения, чтобы получить все подключения определенного типа.

## ПРИМЕРЫ

### Пример 1. Получить все подключения
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

Эта команда получает метаданные для всех подключений в учетной записи автоматизации Contoso17.

### Пример 2. Получить все подключения одного типа
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

Эта команда получает метаданные для подключений в учетной записи автоматизации Contoso17.
Эта команда получает соединения типа SqlServer.

### Пример 3. Подключение
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

Эта команда получает метаданные подключения ContosoConnection.

## PARAMETERS

### -AutomationAccountName
Указывает имя учетной записи автоматизации, для которой этот cmdlet получает подключения.

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

### -ConnectionTypeName
Указывает имя типа подключения, для которого этот cmdlet извлекает соединения.

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
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

### -Name
Указывает имя подключения, которое извлекает этот cmdlet.

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, для которой этот cmdlet получает подключения.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Automation.Model.Connection

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzAutomationConnection](./New-AzAutomationConnection.md)

[Remove-AzAutomationConnection](./Remove-AzAutomationConnection.md)


