---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075741"
---
# Stop-AzureVM

## КРАТКИй обзор
Завершает работу виртуальной машины Azure.

## Максимальное

### ByName (по умолчанию)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Вводим
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Stop-AzureVM** завершает работу виртуальной машины.

## ИЛЛЮСТРИРУЮТ

### Пример 1: отключение виртуальной машины
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

Эта команда завершает работу виртуальной машины, в которой находится указанная служба.

### Пример 2: отключение виртуальной машины с помощью объекта виртуальной машины
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

Эта команда завершает работу виртуальной машины, в которой находится указанная служба, с помощью объекта виртуальной машины, возвращаемого функцией **Get-AzureVM** .

### Пример 3: отключение виртуальной машины и сохранение подготовленной виртуальной машины
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

Эта команда завершает работу виртуальной машины, содержащей указанную службу, и сохраняет ее подготовленную.

### Пример 4: отключение виртуальной машины и разрешение освобождения последней виртуальной машины в развертывании
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

Эта команда завершает работу виртуальной машины, в которой находится указанная служба, и позволяет выделять последнюю виртуальную машину в развертывании.

### Пример 5: Отключение нескольких виртуальных машин
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

Эта команда завершает работу нескольких виртуальных машин, которые содержат указанную службу.

## ПАРАМЕТРЫ

### -Force
Указывает, следует ли разрешить изъятие последней виртуальной машины в развертывании.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -Name (имя)
Указывает имя виртуальной машины, которую нужно выключить.

Используйте подстановочный знак для асинхронной остановки нескольких виртуальных машин.
С подстановочными знаками этот командлет вызывает операцию завершения работы ролей https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) вместо операции завершения работы роли https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx () https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
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

### -ServiceName
Указывает имя службы Azure, которая содержит виртуальную машину, которую нужно завершить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
Указывает на то, что этот командлет обеспечивает сохранение подготовленной виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Указывает объект виртуальной машины, который определяет виртуальную машину для завершения работы.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

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

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[Restarts-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)


