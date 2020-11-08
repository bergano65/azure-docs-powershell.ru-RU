---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076505"
---
# Get-AzureWinRMUri

## КРАТКИй обзор
Получает универсальный код ресурса (URI) для удаленного прослушивателя HTTPS на виртуальную машину или список виртуальных машин в размещенной службе.

## Максимальное

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureWinRMUri** возвращает универсальный код ресурса (URI) прослушивателя HTTPS для удаленного управления Windows (WinRM) на виртуальную машину или список виртуальных машин в размещенной службе.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Получение URI-кода прослушивателя WinRM HTTPS для виртуальной машины
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

Эта команда возвращает UIR прослушивателя HTTPS для WinRM на виртуальную машину.

### Пример 2: Получение URI-кода прослушивателя WinRM HTTPS для виртуальной машины определенной службы
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

Эта команда возвращает UIR прослушивателя HTTPS для WinRM на виртуальную машину.

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
Указывает имя виртуальной машины, для которой создается универсальный код ресурса (URI) WinRM.

```yaml
Type: String
Parameter Sets: (All)
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
Указывает имя службы Microsoft Azure, на которой размещена виртуальная машина.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureVM](./New-AzureVM.md)

[New-AzureQuickVM](./New-AzureQuickVM.md)


