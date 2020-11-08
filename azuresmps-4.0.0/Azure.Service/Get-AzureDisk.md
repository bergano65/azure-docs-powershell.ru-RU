---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076354"
---
# Get-AzureDisk

## КРАТКИй обзор
Получение сведений о дисках в репозитории дисков Azure.

## Максимальное

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureDisk** получает сведения о дисках, которые хранятся в репозитории дисков Azure для текущей подписки.
Этот командлет возвращает список сведений для всех дисков в репозитории.
Чтобы просмотреть сведения о конкретном диске, укажите его имя.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений о диске
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Эта команда возвращает данные о диске с именем ContosoDataDisk из репозитория дисков.

### Пример 2: получение сведений обо всех дисках
```
PS C:\> Get-AzureDisk
```

Эта команда получает сведения обо всех дисках в репозитории дисков.

### Пример 3: получение сведений о диске
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Эта команда получает данные для всех дисков в репозитории дисков, которые в настоящее время не подключены к виртуальной машине.
Команда получает сведения обо всех дисках и передает каждый объект в командлет **Where-Object** .
Этот командлет удаляет диск, для свойства **AttachedTo** которого не задано значение $null.
Команда форматирует список в виде таблицы с помощью командлета **Format-Table** .

## ПАРАМЕТРЫ

### -DiskName
Указывает имя диска в репозитории дисков, для которого этот командлет получает сведения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

[Add-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


