---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076335"
---
# Get-AzureMediaServicesAccount

## КРАТКИй обзор
Получает доступные учетные записи служб мультимедиа Azure.

**Примечание.** Эта версия устарела, ознакомьтесь с [более новой версией](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## Максимальное

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Чтобы вывести все учетные записи, используйте `Get-AzureMediaServicesAccount` командлет.
Чтобы получить более подробные сведения об определенной учетной записи, используйте `Get-AzureMediaServicesAccount -Name YourAccountName` командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех учетных записей служб мультимедиа
```
PS C:\> Get-AzureMediaServicesAccount
```

Эта команда перечисляет все доступные учетные записи служб мультимедиа.

### Пример 2: получение подробных сведений об учетной записи служб мультимедиа
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Эта команда отображает свойства учетной записи служб мультимедиа.

## ПАРАМЕТРЫ

### -Name (имя)
Имя учетной записи службы мультимедиа.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Использование Azure PowerShell для служб мультимедиа](https://go.microsoft.com/fwlink/?LinkId=324179)


