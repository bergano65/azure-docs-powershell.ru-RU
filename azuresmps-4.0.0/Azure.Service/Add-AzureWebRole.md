---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075711"
---
# Add-AzureWebRole

## КРАТКИй обзор
Добавление роли веб-рабочего процесса.

## Максимальное

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Add-AzureWebRole** добавляет роль веб-рабочего процесса.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление роли по умолчанию
```
PS C:\> Add-AzureWebRole
```

Эта команда добавляет веб-роль с конфигурацией по умолчанию Webrole1 в качестве имени и единственного экземпляра.

### Пример 2: Добавление роли с именем
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

Эта команда добавляет одну веб-роль с именем MyWebRole в текущее приложение.

### Пример 3: Добавление роли с именем и количеством экземпляров
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

Эта команда добавляет в текущее приложение веб-роль с именем MyWebRole.
Число экземпляров роли в командлете равно 2.

### Пример 4: Добавление роли с именем и шаблоном
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

Эта команда добавляет одну веб-роль с именем MyWebRole в текущее приложение.
Команда задает папку с именем MyWebTemplateFolder в качестве шаблона формирования шаблонов.

## ПАРАМЕТРЫ

### -Экземпляры
Указывает количество экземпляров.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя веб-роли.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -TemplateFolder
Указывает папку шаблонов.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


