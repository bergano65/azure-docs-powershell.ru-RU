---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076387"
---
# Add-AzurePHPWorkerRole

## КРАТКИй обзор
Создает необходимые файлы и конфигурацию для приложения PHP, которое будет размещено в Azure с помощью php.exe.

## Максимальное

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Создает необходимые файлы и конфигурацию, иногда называемые формированием шаблонов, для приложения PHP, которое будет размещено в Azure с помощью php.exe.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание рабочей роли с одним экземпляром
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

В этом примере в текущее приложение добавляются необходимые файлы и конфигурация для одной роли рабочего процесса с именем MyWorkerRole.

### Пример 2: Создание роли рабочего процесса с несколькими экземплярами
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

В этом примере в текущее приложение добавляются необходимые файлы и параметры для новой рабочей роли, используя имя MyWorkerRole с числом экземпляров роли 2.

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
Имя определяет имя папки, которая включает необходимые файлы и конфигурацию для службы PHP, размещенной в рабочей роли.
Значение по умолчанию — WorkerRole1.

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

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


