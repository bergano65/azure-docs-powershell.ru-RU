---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559599"
---
# New-AzureRmNotificationHub

## КРАТКИй обзор
Создает концентратор уведомлений.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### InputFileParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmNotificationHub** создает концентратор уведомлений.
Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.
Концентраторы уведомлений примерно эквивалентны отдельным приложениям: каждое из ваших приложений обычно имеет собственный концентратор уведомлений.

Командлет **New-AzureRmNotificationHub** предоставляет два способа создания нового концентратора уведомлений.
Вы можете создать экземпляр объекта **NotificationHubAttributes** , а затем настроить этот объект.
Затем вы можете скопировать значения этих свойств в новый центр с помощью параметра *NotificationHubObj* .

Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .

При использовании в сочетании с командлетом **New-AzureRmNotificationHub** в ПРЕДЫДУЩЕМ примере JSON создается центр уведомлений под названием ContosoNotificationHub, который находится в центре обработки данных "Западная часть США".

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание концентратора уведомлений
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Эта команда создает концентратор уведомлений в пространстве имен ContosoNamespace.
Новая ступица будет назначена ContosoNotificationsGroup.
Вам не нужно указывать имя или какие-либо другие сведения о конфигурации для концентратора; Эти данные будут взяты из входного файла, C:\Configurations\InternalHub.jsвключены.

## ПАРАМЕТРЫ

### -InputFile
Задает путь к файлу JSON, содержащему значения конфигурации для нового концентратора уведомлений.

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
Задает пространство имен, которому будет назначен Центр уведомлений.

Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.
Концентраторы уведомлений должны быть назначены существующему пространству имен.
Командлет **New-AzureRmNotificationHub** не может создать новое пространство имен.

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

### -NotificationHubObj
Указывает объект **NotificationHubAttributes** , содержащий сведения о конфигурации для нового концентратора.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Указывает группу ресурсов, которой будет назначен концентратор уведомлений.
Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.

Необходимо использовать существующую группу ресурсов.
Командлет **New-AzureRmNotificationHub** не может создать новую группу ресурсов.

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

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmNotificationHub](./Get-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Set-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


