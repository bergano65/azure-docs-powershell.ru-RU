---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076066"
---
# Set-AzureDataDisk

## КРАТКИй обзор
Изменяет кэширование узла для существующего диска с данными на виртуальной машине Azure.

## Максимальное

### NoResize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Изменение размера
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureDataDisk** изменяет атрибуты кэша для существующего диска с данными на виртуальной машине Azure.
Укажите, какой диск данных нужно обновить по его логическому номеру устройства (LUN).

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение кэширования узла для диска данных
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Эта команда получает виртуальные машины, которые выполняются в службе с именем ContosoService, с помощью командлета **Get-AzureVM** .
Команда передает их в текущий командлет с помощью оператора конвейера.
Этот командлет задает диск данных на LUN 2 виртуальной машины с именем VirtualMachine07, чтобы использовать кэширование узлов только для чтения.
Команда обновляет виртуальную машину, отображая изменения с помощью командлета **Update-AzureVM** .

### Пример 2: изменение кэширования узла для всех дисков данных на виртуальной машине
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Эта команда получает объект для виртуальной машины с именем VirtualMachine07 в облачной службе ContosoService.
Команда передается командлету **Get-AzureDataDisk** , который получает диски данных для виртуальной машины.
Затем текущий командлет задает режим кэширования узла для всех дисков с данными в ReadWrite.
Команда обновит виртуальную машину, чтобы отразить ваши изменения.

## ПАРАМЕТРЫ

### -DiskName
Указывает имя конфигурации диска данных, которую изменяет этот командлет.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> Кэширование диска не поддерживается для дисков 4 TiB и более крупных. Если к ВМ подключено несколько дисков, то каждый из дисков, размер которых меньше 4 TiB, будет поддерживать кэширование.
>
> Изменение параметра кэша диска Azure отсоединяет и повторно подключает конечный диск. Если это диск операционной системы, виртуальная машина перезапускается. Перед изменением параметров кэша дисков Остановите все приложения и службы, которые могут повлиять на этот перерыв. Отсутствие подписки на эти рекомендации может привести к повреждению данных.

Задает параметры кэширования на уровне узла для диска.
Допустимые значения:

- Ничего
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

### -LUN
Указывает LUN для диска данных в виртуальной машине.
Допустимые значения: от 0 до 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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
Указывает новый размер (в гигабайтах) для диска с данными.
Новый размер должен быть больше текущего размера.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Указывает объект виртуальной машины, прикрепленный к диску данных.
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

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


