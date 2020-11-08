---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075759"
---
# Suspend-AzureAutomationJob

## КРАТКИй обзор

Приостанавливает задание автоматизации.

## Максимальное

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Командлет **Suspend-AzureAutomationJob** приостанавливает задание службы автоматизации Microsoft Azure.
Укажите выполнение задания автоматизации.

Чтобы возобновить приостановленное задание, используйте командлет **Resume-AzureAutomationJob** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Приостановка задания
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

Эта команда приостанавливает задание с указанным ИДЕНТИФИКАТОРом.

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Указывает идентификатор задания.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureAutomationJob](./Get-AzureAutomationJob.md)

[Возобновить — AzureAutomationJob](./Resume-AzureAutomationJob.md)

[Остановить-AzureAutomationJob](./Stop-AzureAutomationJob.md)


