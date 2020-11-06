---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: 45e61b79381cc9acddf4dc12c5d8e905627130a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562340"
---
# Set-AzureRmNotificationHub

## КРАТКИй обзор
Задает значения свойств для центра уведомлений.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### InputFileParameterSet
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmNotificationHub** изменяет значения свойств в центре уведомлений.

Значение свойства "Центр уведомлений" можно изменить двумя способами.
Для одного из них вы можете создать экземпляр объекта **NotificationHubAttributes** , а затем настроить этот объект с помощью значений свойств, которыми должен обладать новый концентратор.
Это можно сделать с помощью .NET Framework.
Затем можно скопировать значения этих свойств в центр с помощью параметра *NotificationHubObj* .

Кроме того, вы можете создать файл JSON (объектная нотация JavaScript), содержащий соответствующие значения конфигурации, а затем применить эти значения через параметр *inputFile* .
JSON-файл — это текстовый файл, который использует синтаксис, аналогичный приведенному ниже.

{  
    "Имя": "ContosoNotificationHub";  
    "Расположение": "Западная часть США",  
}

При использовании в сочетании с командлетом **Set-AzureRmNotificationHub** предыдущий пример JSON задает значение Location для концентратора уведомлений с именем ContosoNotificationHub на запад US.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение значений свойств для центра уведомлений
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

Эта команда изменяет значения свойств для центра уведомлений, найденного в пространстве имен ContosoNamespace, и назначает его группе ресурсов ContosoNotificationsGroup.
Значения свойства, а также имя узла, который нужно изменить, не указываются в команде.
Вместо этого информация, содержащаяся в файле ввода, C:\Configuration\Hubs.jsвключена.

## ПАРАМЕТРЫ

### -Force
Не запрашивать подтверждение.

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

### -InputFile
Задает путь к файлу JSON, содержащему сведения о конфигурации для центра уведомлений.

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
Задает пространство имен, которому назначен Центр уведомлений.
Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.

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
Указывает объект **NotificationHubAttributes** , который содержит сведения о конфигурации для основного центра, измененного этим командлетом.

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
Указывает группу ресурсов, которой назначен Центр уведомлений.
Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.

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

[New-AzureRmNotificationHub](./New-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)


