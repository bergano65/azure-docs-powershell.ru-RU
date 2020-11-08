---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075992"
---
# New-AzureRoleTemplate

## КРАТКИй обзор
Создает шаблоны веб-и рабочих ролей.

## Максимальное

### Роль "Администратор"
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **New-AzureRoleTemplate** создает шаблоны веб-роли и рабочих ролей.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание шаблона веб-роли
```
PS C:\> New-AzureRoleTemplate -Web
```

В этом примере создается новый шаблон веб-роли в папке с именем WebRoleTemplate в текущем каталоге.

### Пример 2: Создание шаблона рабочей роли
```
PS C:\> New-AzureRoleTemplate -Worker
```

В этом примере создается новый шаблон рабочей роли в папке с именем WebRoleTemplate в текущем каталоге.

### Пример 3: Создание шаблона роли в настраиваемом каталоге
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

В этом примере создается новый шаблон веб-роли в каталоге с именем MyWebRoleTemplate, а не в текущем каталоге.

## ПАРАМЕТРЫ

### -Output
Указывает путь вывода для созданного шаблона.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Веб-сайт
Указывает, что вы хотите создать шаблон веб-роли.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Исполнитель
Указывает, что вы хотите создать шаблон роли рабочего процесса.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)


