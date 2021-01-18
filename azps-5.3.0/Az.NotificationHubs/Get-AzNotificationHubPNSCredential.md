---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519854"
---
# Get-AzNotificationHubPNSCredential

## SYNOPSIS
Получает учетные данные PNS для концентратора уведомлений.

## СИНТАКСИС

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzNotificationHubPNSCredential** получает учетные данные службы уведомлений платформы (PNS) для концентратора уведомлений.
Каждый концентратор уведомлений имеет один набор учетных данных PNS.
Эти учетные данные применяются к отдельным службам push-уведомлений, таким как: служба push-уведомлений iOS, служба push-уведомлений Android и Windows Phone 8.

## ПРИМЕРЫ

### Пример 1. Получить учетные данные PNS для определенного концентратора уведомлений
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Эта команда получает учетные данные PNS для концентратора уведомлений ContosoInternalHub, который принадлежит к группе ресурсов ContosoNotificationsGroup.

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

### -Namespace
Определяет пространство имен, которому назначен концентратор уведомлений.
Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.

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

### -NotificationHub
Указывает центр уведомлений, для который назначены учетные данные PNS.
Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Группа ресурсов, которой назначен концентратор уведомлений.
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHub](./Get-AzNotificationHub.md)


