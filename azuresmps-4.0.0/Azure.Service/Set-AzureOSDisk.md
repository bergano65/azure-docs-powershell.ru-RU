---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075828"
---
# Set-AzureOSDisk

## КРАТКИй обзор
Изменение режима кэширования узла для виртуальной машины Azure.

## Максимальное

### NoResize
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Изменение размера
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureOSDisk** изменяет режим кэширования хоста на диске операционной системы виртуальной машины Azure.
Поддерживаемые режимы кэширования узла: ReadOnly и ReadWrite.
Если запустить этот командлет на работающей виртуальной машине, эта виртуальная машина будет перезапущена.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка режима кэширования узла на ReadOnly с помощью конвейера
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

Эта команда получает виртуальную машину с именем VirtualMachine02 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .
Команда передает виртуальную машину в текущий командлет с помощью оператора конвейера.
Текущий командлет устанавливает режим кэширования на диске операционной системы для виртуальной машины на ReadOnly.

### Пример 2: Настройка режима кэширования узла на ReadWrite
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

Первая команда получает виртуальную машину с именем VirtualMachine02 в службе с именем ContosoService и сохраняет ее в переменной.

Вторая команда задает в качестве режима кэширования на диске операционной системы для виртуальной машины значение ReadWrite.

## ПАРАМЕТРЫ

### -HostCaching
Задает атрибут кэша узла для диска с операционной системой.
Допустимые значения: 

- Чтения 
- Операцию

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
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

### -ResizedSizeInGB
Указывает новый размер (в гигабайтах) для диска операционной системы.
Размер должен быть больше текущего размера.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Указывает виртуальную машину, для которой этот командлет изменяет диск операционной системы.
Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureOSDisk](./Get-AzureOSDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


