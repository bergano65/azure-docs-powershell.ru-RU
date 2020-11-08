---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075735"
---
# Add-AzureDataDisk

## КРАТКИй обзор
Добавляет диск с данными на виртуальную машину.

## Максимальное

### CreateNew (по умолчанию)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Импортируем
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureDataDisk** добавляет новый или существующий диск данных в объект виртуальной машины Azure.
С помощью параметра *CreateNew* создайте новый диск с данными, который содержит заданные размер и метку.
С помощью параметра *Import* вы можете подключить существующий диск из репозитория изображений.
Используйте параметр *ImportFrom* , чтобы присоединить существующий диск из большого двоичного объекта в учетной записи хранения.
Вы можете указать режим кэширования хост-данных для подключенного диска с данными.

## ИЛЛЮСТРИРУЮТ

### Пример 1: импорт диска с данными из репозитория
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Эта команда получает объект виртуальной машины для виртуальной машины с именем VirtualMachine07 в облачной службе ContosoService с помощью командлета **Get-AzureVM** .
Команда передается текущему командлету с помощью оператора конвейера.
Эта команда подключает существующий диск с данными из репозитория к виртуальной машине.
Диск с данными имеет LUN 0.
Команда обновляет виртуальную машину, отображая изменения с помощью командлета **Update-AzureVM** .

### Пример 2: Добавление нового диска с данными
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Эта команда получает объект виртуальной машины для виртуальной машины с именем VirtualMachine08.
Команда передается текущему командлету.
Эта команда прикрепляет новый диск с данными с именем MyNewDisk. VHD.
Командлет создает диск в контейнере виртуальных жестких дисков в учетной записи хранения по умолчанию текущей подписки.
Команда обновит виртуальную машину, чтобы отразить ваши изменения.

### Пример 3: Добавление диска с данными из указанного места
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Эта команда получает объект виртуальной машины для виртуальной машины с именем Database.
Команда передается текущему командлету.
Эта команда подключает существующий диск данных с именем Disk14. VHD из указанного места.
Команда обновит виртуальную машину, чтобы отразить ваши изменения.

## ПАРАМЕТРЫ

### -CreateNew
Указывает на то, что этот командлет создает диск с данными.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Указывает метку диска для нового диска с данными.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskName
Указывает имя диска данных в репозитории дисков.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Задает размер логического диска (в гигабайтах) для нового диска с данными.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Задает параметры кэширования на уровне узла для диска.
Допустимые значения: 

- Ничего 
- Чтения 
- Операцию

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Import
Указывает на то, что этот командлет импортирует существующий диск с данными из репозитория изображений.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Указывает на то, что этот командлет импортирует существующий диск с данными из большого двоичного объекта в учетной записи хранения.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
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
Задает логический номер устройства (LUN) для диска данных в виртуальной машине.
Допустимые значения: от 0 до 15.
Каждый диск данных должен иметь уникальный LUN.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Указывает расположение большого двоичного объекта в учетной записи хранения Azure, в котором этот командлет хранит диск данных.
Если расположение не задано, командлет сохраняет диск данных в контейнере VHDs в учетной записи хранения по умолчанию для текущей подписки.
Если контейнер виртуальных жестких дисков не существует, командлет создает контейнер виртуальных жестких дисков.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
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

### -VM
Указывает объект виртуальной машины, к которому этот командлет прикрепляет диск данных.
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

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


