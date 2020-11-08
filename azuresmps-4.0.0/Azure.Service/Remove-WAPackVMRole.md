---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077411"
---
# Remove-WAPackVMRole

## КРАТКИй обзор
Удаляет объекты роли виртуальной машины.

## Максимальное

### FromVMRoleObject (по умолчанию)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Эти разделы устарели и будут исключены в будущем.
В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.
Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Remove-WAPackVMRole** удаляет объекты роли виртуальной машины.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление роли виртуальной машины (созданной с помощью портала WAP)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

Первая команда получает роль виртуальной машины с именем ContosoVMRole01 с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.

Вторая команда удаляет роль виртуальной машины, хранящуюся в $VMRole.
В командной строке появится запрос на подтверждение. Если вы предполагают, что эта роль виртуальной машины была создана с помощью портала WAP, вам не нужно указывать имя облачной службы.

### Пример 2: Удаление роли виртуальной машины, созданной после создания облачной службы вручную
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

Первая команда получает роль виртуальной машины с именем "ContosoVMRole02" с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.

Вторая команда удаляет роль виртуальной машины, хранящуюся в $VMRole.
В командной строке появится запрос на подтверждение.
Если вы предполагают, что эта роль виртуальной машины не была создана с помощью портала, пользователю необходимо указать имя облачной службы.
В этом случае с именем "ContosoCloudService02".

### Пример 3: Удаление роли виртуальной машины без подтверждения
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

Первая команда получает облачную службу с именем ContosoVMRole03 с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.

Вторая команда удаляет роль виртуальной машины, хранящуюся в $VMRole.
Эта команда включает параметр *Force* .
Команда не запрашивает подтверждение.

## ПАРАМЕТРЫ

### -CloudServiceName
Указывает имя облачной службы для роли виртуальной машины.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -VMRole
Указывает роль виртуальной машины.
Чтобы получить роль виртуальной машины, используйте командлет **Get-WAPackVMRole** .

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[New-WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


