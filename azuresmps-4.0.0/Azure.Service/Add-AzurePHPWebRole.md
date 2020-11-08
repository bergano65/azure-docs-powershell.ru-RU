---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076390"
---
# Add-AzurePHPWebRole

## КРАТКИй обзор
Создает необходимые файлы и конфигурацию для приложения PHP.

## Максимальное

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Add-AzurePHPWebRole** создает файлы и конфигурацию, иногда называемые формированием шаблонов, для приложения PHP, которое будет размещено в Azure через IIS.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление веб-роли с использованием значений по умолчанию
```
PS C:\> Add-AzurePHPWebRole
```

В этом примере добавляются необходимые файлы и конфигурация для новой веб-роли с использованием значений по умолчанию для службы с именем "WebRole1" с 1 экземпляром.

### Пример 2: Добавление веб-роли с несколькими экземплярами
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

В этом примере в текущее приложение добавляются необходимые файлы и конфигурация для новой веб-роли с именем "MyWebRole", а количество экземпляров роли — 2.

## ПАРАМЕТРЫ

### -Экземпляры
Задает количество экземпляров ролей для этой веб-роли.
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
Указывает имя веб-роли.
Имя определяет имя каталога, содержащего необходимые файлы и конфигурацию для приложения PHP.
По умолчанию используется значение #, где # — количество веб-ролей в службе.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


