---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076389"
---
# Add-AzureNodeWorkerRole

## КРАТКИй обзор
Создание необходимых файлов и папок для приложения Node.js, которое будет размещено в облаке с помощью node.exe

## Максимальное

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Add-AzureNodeWorkerRole** создает необходимые файлы и папки, которые иногда называют механизмом формирования шаблонов, для того чтобы приложение Node.js было размещено в облаке с помощью node.exe.

## ИЛЛЮСТРИРУЮТ

### Пример 1: роль рабочего процесса с одним экземпляром
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

В этом примере в текущее приложение добавляется формирование шаблонов для одной роли рабочего процесса с именем **MyWorkerRole** .

### Пример 2: Рабочая роль для нескольких экземпляров
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

В этом примере для одной рабочей роли с именем **MyWorkerRole** в текущее приложение добавляется формирование шаблонов с числом экземпляров роли 2.

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
Значение определяет имя папки, содержащей формирование шаблонов для службы node.js, размещенной в рабочей роли.
По умолчанию используется WorkerRole1.

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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


