---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240485"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Создает правило авторизации и назначает его области имен концентратора уведомлений.

## СИНТАКСИС

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания правила авторизации saS создается правило авторизации SAS с новыми **именамиHubsNamespaceAuthorizationRule** и назначается пространство имен концентратора уведомлений.
Правила авторизации управляют правами пользователей на пространство имен и в концентраторы уведомлений, содержащиеся в этом пространстве имен.
Этот cmdlet предоставляет два способа создать новое правило авторизации и назначить его в область имен.
Вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes,** а затем настроить этот объект со значениями свойств, которые будут иметь новое правило.
Это можно сделать с помощью .NET Framework.
Затем эти значения свойств можно скопировать в новое правило с помощью *параметра SASRule.*
Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, а затем применить их с помощью параметра *InputFile.*
JSON-файл — это текстовый файл с синтаксисом, аналогичным следующему: {  
    "Name": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXj извещенt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Права": \[  
        "Прослушивание",  
        "Отправить"  
    \]  
} При использовании в сочетании с cmdlet **new-AzNotificationHubsNamespaceAuthorizationRule,** в предыдущем примере JSON создается правило авторизации с именем ContosoAuthorizationRule, которое предоставляет пользователям права на прослушивание и отправку прав в пространство имен.
*Первичныйkey,* используемый для проверки подлинности, может быть случайным образом создан с помощью следующей команды Windows PowerShell: \[ Convert \] ::ToBase64String((1,32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))

## ПРИМЕРЫ

### Пример 1. Создание правила авторизации и назначение его области имен
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Эта команда создает правило авторизации и назначает его области имен ContosoNamespace.
При создании этого правила необходимо указать соответствующее пространство имен и группу ресурсов, которая назначена этому пространству.
Однако указывать какие-либо сведения о правиле не требуется: сведения о правиле будут взяты из входного файла, C:\Configuration\NamespaceAuthorizationRules.js.

## PARAMETERS

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

### -InputFile
Путь к файлу JSON, содержащего сведения о конфигурации для нового правила авторизации.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Определяет пространство имен, в которое будут назначены правила авторизации.
Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.
Новые правила должны быть назначены существующему пространству имен.
Для **создания нового пространства имен нельзя** создать новое пространство имен.

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

### -ResourceGroup
Группа ресурсов, которой назначено пространство имен.
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.
Необходимо использовать существующую группу ресурсов.
Этот cmdlet не может создать новую группу ресурсов.

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

### -SASRule
Определяет объект **SharedAccessAuthorizationRuleAttributes,** содержащий сведения о конфигурации для новых правил.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


