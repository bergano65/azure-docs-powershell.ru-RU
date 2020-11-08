---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077400"
---
# New-WAPackQuickVM

## КРАТКИй обзор
Создание виртуальной машины на основе шаблона.

## Максимальное

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Эти разделы устарели и будут исключены в будущем.
В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.
Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **New-WAPackQuickVM** создает виртуальную машину на основе шаблона.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание виртуальной машины на основе шаблона
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

Для первой команды создается объект **PSCredential** , который затем сохраняется в переменной $Credentials.
Командлет запрашивает учетные записи и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

Вторая команда получает шаблон с помощью командлета **Get-WAPackVMTemplate** .
Команда задает идентификатор шаблона.
Команда сохраняет объект шаблона в переменной $TemplateID.

Последняя команда создает виртуальную машину с именем VirtualMachine023.
Команда помещает виртуальную машину в шаблон, хранящийся в $TemplateId.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя виртуальной машины.

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

### -Template
Задает шаблон.
Командлет создает виртуальную машину на основе указанного шаблона.
Чтобы получить объект шаблона, используйте командлет **Get-WAPackVMTemplate** .

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Задает учетные данные для учетной записи локального администратора.
Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
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

[New-WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


