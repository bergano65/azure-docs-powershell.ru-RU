---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077407"
---
# Remove-WAPackVMSubnet

## КРАТКИй обзор
Удаляет объекты подсети виртуальной машины.

## Максимальное

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Эти разделы устарели и будут исключены в будущем.
В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.
Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Remove-WAPackVMSubnet** удаляет объекты подсети виртуальной машины.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление подсети виртуальной машины
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

Первая команда получает подсеть виртуальной машины с именем ContosoVMSubnet01 с помощью командлета **Get-WAPackVMSubnet** и сохраняет этот объект в переменной $VMSubnet.

Вторая команда удаляет подсеть виртуальной машины, хранящуюся в $VMSubnet.
В командной строке появится запрос на подтверждение.

### Пример 2: Удаление виртуальной машины без подтверждения
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

Первая команда получает облачную службу с именем ContosoVMSubnet02 с помощью командлета **Get-WAPackVMSubnet** , а затем сохраняет этот объект в переменной $VMSubnet.

Вторая команда удаляет подсеть виртуальной машины, хранящуюся в $VMSubnet.
Эта команда включает параметр *Force* .
Команда не запрашивает подтверждение.

## ПАРАМЕТРЫ

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает объект, который представляет собой элемент, с которым вы работаете.
По умолчанию этот командлет не создает никаких выходных данных.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

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

### -VMSubnet
Указывает подсеть виртуальной машины.
Чтобы получить подсеть виртуальной машины, используйте командлет **Get-WAPackVMSubnet** .

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[New-WAPackVMSubnet](./New-WAPackVMSubnet.md)


