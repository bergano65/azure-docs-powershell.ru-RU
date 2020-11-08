---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076547"
---
# Get-AzureVM

## КРАТКИй обзор
Получение сведений из одной или нескольких виртуальных машин Azure.

## Максимальное

### ListAllVMs (по умолчанию)
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureVM** извлекает сведения о виртуальных машинах, работающих в Azure.
Он возвращает объект со сведениями о конкретной виртуальной машине или, если виртуальная машина не указана, для всех виртуальных машин в указанной службе текущей подписки.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений об указанной виртуальной машине
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

Эта команда возвращает объект со сведениями о виртуальной машине VirtualMachine02, работающей в облачной службе ContosoService01.

### Пример 2: получение сведений на всех виртуальных машинах
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

Эта команда извлекает объект List со сведениями обо всех виртуальных машинах, запущенных в облачной службе ContosoService01.

### Пример 3: отображение таблицы состояния виртуальных машин
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

Эта команда отображает таблицу, в которой показаны виртуальные машины, запущенные в службе ContosoService01, их домен обновления, а также текущее состояние каждой виртуальной машины.

## ПАРАМЕТРЫ

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
Указывает имя виртуальной машины, для которой требуется получить сведения.
Если этот параметр не указан, командлет возвращает объект List со сведениями обо всех виртуальных машинах в указанной службе.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
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
Указывает имя облачной службы, для которой требуется возвратить сведения о виртуальной машине.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
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

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzureVM](./Remove-AzureVM.md)

[Restarts-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)

[Stop-AzureVM](./Stop-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


