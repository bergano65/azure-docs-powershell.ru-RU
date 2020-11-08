---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077398"
---
# New-WAPackVM

## КРАТКИй обзор
Создание виртуальной машины.

## Максимальное

### CreateVMFromTemplate (по умолчанию)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Эти разделы устарели и будут исключены в будущем.
В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.
Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **New-WAPackVM** создает виртуальную машину.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание виртуальной машины для операционной системы Windows с помощью шаблона
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

Для первой команды создается объект **PSCredential** , который затем сохраняется в переменной $Credentials.
Командлет запрашивает учетные записи и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

Вторая команда получает шаблон виртуальной машины с именем ContosoTemplate04 с помощью командлета **Get-WAPackVMTemplate** и сохраняет его в переменной $Template.

Последняя команда создает виртуальную машину с именем ContosoV023 в соответствии с шаблоном, хранящимся в переменной $Template.
В команде указан параметр *Windows* , поэтому виртуальная машина должна запустить версию операционной системы Windows.

### Пример 2: создание виртуальной машины для операционной системы Linux с помощью шаблона
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

Для первой команды создается объект **PSCredential** , который затем сохраняется в переменной $Credentials.

Вторая команда получает шаблон виртуальной машины с именем ContosoTemplate19 с помощью командлета **Get-WAPackVMTemplate** и сохраняет его в переменной $Template.

Последняя команда создает виртуальную машину с именем ContosoV028 в соответствии с шаблоном, хранящимся в переменной $Template.
В команде указан параметр *Linux* , поэтому виртуальная машина должна использовать версию операционной системы Linux.

### Пример 3: создание виртуальной машины на диске и в профиле размера операционной системы
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

Первая команда получает диск операционной системы с именем ContosoDiskOS с помощью командлета **Get-WAPackVMOSDisk** и сохраняет его в переменной $OSDisk.

Вторая команда получает профиль размера с именем MediumSizeVM с помощью командлета **Get-WAPackVMSizeProfile** , а затем сохраняет его в переменной $SizeProfile.

Последняя команда создает виртуальную машину с именем ContosoV073 с диска операционной системы, хранящейся в $OSDisk, и профиль размера, хранящийся в $SizeProfile.

## ПАРАМЕТРЫ

### -AdministratorSSHKey
Задает ключ безопасной оболочки (SSH) для учетной записи администратора.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Указывает на то, что командлет создает виртуальную машину для запуска операционной системы Linux.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSDisk
Указывает диск операционной системы как объект **VirtualHardDisk** .
Чтобы получить диск операционной системы, используйте командлет **Get-WAPackVMOSDisk** .

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Задает ключ продукта.
Ключ продукта — это 25-значный номер, обозначающий лицензию на продукт.
Используйте ключ продукта для операционной системы, которую вы планируете установить на виртуальной машине или узле.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
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

### -Template
Задает шаблон.
Командлет создает виртуальную машину на основе указанного шаблона.
Чтобы получить объект шаблона, используйте командлет Get-WAPackVMTemplate.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Задает учетные данные для учетной записи локального администратора.
Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Задает в качестве объекта **HardwareProfile** профиль размера для виртуальной машины.
Чтобы получить профиль размера, используйте командлет **Get-WAPackVMSizeProfile** .

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Указывает виртуальную сеть.
Командлет подключается к виртуальной машине в указанную вами виртуальную сеть.
Чтобы получить виртуальную сеть, используйте командлет **Get-WAPackVNet** .

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Указывает на то, что командлет создает виртуальную машину для запуска операционной системы Windows.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
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

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restarting-WAPackVM](./Restart-WAPackVM.md)

[Возобновить — WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Start-WAPackVM](./Start-WAPackVM.md)

[Остановить-WAPackVM](./Stop-WAPackVM.md)

[Приостановить — WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


