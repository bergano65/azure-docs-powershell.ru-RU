---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 6a55a1b6b032bf2354d7d88699744f9cc5dbaea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564187"
---
# New-AzureRmNotificationHubsNamespaceAuthorizationRules

## КРАТКИй обзор
Создает правило авторизации и назначает это правило пространству имен концентратора уведомлений.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### InputFileParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmNotificationHubsNamespaceAuthorizationRules** создает правило авторизации для общего доступа к подписи (SAS) и назначает его пространству имен концентратора уведомлений.
Правила авторизации управляют правами пользователей на пространство имен и на концентраторы уведомлений, содержащиеся в этом пространстве имен.
Этот командлет предоставляет два способа создания нового правила авторизации и назначения его пространству имен.
Вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes** , а затем настроить этот объект с помощью значений свойств, которым должно обладать новое правило.
Это можно сделать с помощью .NET Framework.
Затем вы можете скопировать значения этих свойств в новое правило с помощью параметра *SASRule* .
Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .
JSON-файл — это текстовый файл, который использует синтаксис, аналогичный приведенному ниже.  
    "Имя": "ContosoAuthorizationRule";  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
    "Права": \[  
        "Прослушать",  
        Отправить  
    \]  
} При использовании в сочетании с командлетом **New-AzureRmNotificationHubsNamespaceAuthorizationRules** предыдущий пример JSON создает правило авторизации с именем ContosoAuthorizationRule, которое дает пользователям возможность прослушивать и отправлять права в пространство имен.
Значение *PrimaryKey* , используемое для проверки подлинности, может быть сгенерировано случайным образом с помощью следующей команды Windows PowerShell: \[ Convert \] :: ToBase64String ((1.. 32 |% { \[ Byte/] (Get-Minimum-минимум 0-Maximum 255)}))

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание правила авторизации и назначение его пространству имен
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Эта команда создает правило авторизации и назначает это правило для пространства имен ContosoNamespace.
При создании этого правила необходимо указать соответствующее пространство имен и группу ресурсов, которой назначено пространство имен.
Однако вам не нужно указывать сведения о правиле: сведения о правиле будут взяты из входного файла C:\Configuration\NamespaceAuthorizationRules.json.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -InputFile
Задает путь к файлу JSON, содержащему сведения о конфигурации для нового правила авторизации.

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
Задает пространство имен, которому будут назначены правила авторизации.
Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.
Новые правила должны быть назначены существующему пространству имен.
Командлет **New-AzureRmNotificationHubsNamespaceAuthorizationRules** не может создать новое пространство имен.

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
Указывает группу ресурсов, которой назначено пространство имен.
Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.
Необходимо использовать существующую группу ресурсов.
Этот командлет не может создать новую группу ресурсов.

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
Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для новых правил.

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


