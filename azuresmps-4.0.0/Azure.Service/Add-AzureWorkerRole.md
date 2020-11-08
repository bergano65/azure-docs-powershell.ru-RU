---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075710"
---
# Add-AzureWorkerRole

## КРАТКИй обзор
Создает необходимые файлы и конфигурацию для настраиваемой рабочей роли.

## Максимальное

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Add-AzureWorkerRole** создает необходимые файлы и конфигурацию, иногда называемые формированием шаблонов, для настраиваемой рабочей роли.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание рабочей роли для одного экземпляра
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

В этом примере в текущее приложение добавляется формирование шаблонов для одной роли рабочего процесса с именем MyWorkerRole.

### Пример 2: создание рабочей роли для нескольких экземпляров
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

Этот пример добавляет формирование шаблонов для новой рабочей роли с именем MyWorkerRole в текущее приложение с количеством экземпляров роли 2.

### Пример 3: Создание роли сотрудника с настраиваемым формированием шаблонов
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

В этом примере создается рабочая роль с настраиваемым формированием шаблонов.

## ПАРАМЕТРЫ

### -Экземпляры
Задает количество экземпляров ролей для этой роли рабочего процесса.
Значение по умолчанию — 1.

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
Указывает имя рабочей роли.
Это значение определяет имя папки, содержащей формирование шаблонов для настраиваемого приложения, которое будет размещено в рабочей роли.
По умолчанию используется WorkerRolenumber, где число — количество рабочих ролей в службе.

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
Указывает папку шаблонов формирования шаблонов, которая будет использоваться для создания рабочей роли.

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

[Add-AzureWebRole](./Add-AzureWebRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


