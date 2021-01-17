---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328414"
---
# Get-AzAutomationCredential

## SYNOPSIS
Получает учетные данные автоматизации.

## СИНТАКСИС

### ByAll (по умолчанию)
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzAutomationCredential** получает одну или несколько учетных данных автоматизации Azure.
По умолчанию возвращаются все учетные данные.
Укажите имя учетных данных для получения определенных учетных данных.
В целях безопасности этот cmdlet не возвращает пароли учетных данных.

## ПРИМЕРЫ

### Пример 1. Получить все учетные данные
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

Эта команда получает метаданные для всех учетных данных в учетной записи автоматизации Contoso17.

### Пример 2. Получить учетные данные
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

Эта команда получает метаданные для учетных данных ContosoCredential в учетной записи автоматизации Contoso17.

## PARAMETERS

### -AutomationAccountName
Указывает имя учетной записи автоматизации, для которой этот cmdlet извлекает учетные данные.

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

### -Name
Указывает имя извлечения учетных данных.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов, для которой этот cmdlet извлекает учетные данные.

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

### Microsoft.Azure.Commands.Automation.Model.CredentialInfo

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzAutomationCredential](./New-AzAutomationCredential.md)

[Remove-AzAutomationCredential](./Remove-AzAutomationCredential.md)

[Set-AzAutomationCredential](./Set-AzAutomationCredential.md)


