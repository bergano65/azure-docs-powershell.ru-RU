---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076392"
---
# Add-AzureNodeWebRole

## КРАТКИй обзор
Создание необходимых файлов и папок для приложения Node.js.

## Максимальное

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

**Надстройка Add-AzureNodeWebRole** создает необходимые файлы и папки, которые иногда называют обоснованными, для того чтобы приложение Node.js было размещено в облаке через IIS.

## ИЛЛЮСТРИРУЮТ

### Пример 1: веб-роль «один экземпляр»
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

В этом примере в текущее приложение добавляется формирование шаблонов для одной веб-роли с именем **MyWebRole** .

### Пример 2: веб-роль для нескольких экземпляров
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

В этом примере добавляется формирование шаблонов для новой веб-роли с именем **MyWebRole** в текущее приложение с количеством экземпляров роли 2.

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
Кроме того, он определяет имя каталога, содержащего формирование шаблонов для приложения node.js, которое будет размещаться в веб-роли.
По умолчанию используется значение #, где # указывает количество веб-ролей в службе.

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

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


