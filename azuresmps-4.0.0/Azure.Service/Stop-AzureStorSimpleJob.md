---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076012"
---
# Stop-AzureStorSimpleJob

## КРАТКИй обзор
Остановка задания StorSimple.

## Максимальное

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Stop-AzureStorSimpleJob** останавливает выполнение задания StorSimple.
Вы можете указать задания, указав идентификатор экземпляра или имя задания.

## ИЛЛЮСТРИРУЮТ

### Пример 1: остановка заданий для устройства
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Эта команда получает задания для устройства с именем Device07 с помощью командлета **Get-AzureStorSimpleJob** .
Команда передает задания в текущий командлет с помощью оператора конвейера.
Текущий командлет останавливает все задания, передаваемые ей командой.
Команда задает параметр *Force* и, таким образом, не запрашивает подтверждение перед тем, как остановить задание.

### Пример 2: остановка определенного задания
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Эта команда останавливает задание с указанным ИДЕНТИФИКАТОРом экземпляра.

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

### -InstanceId
Указывает ИД задания для устройства, которое нужно остановить.

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

### -Profile
Указывает профиль Azure.

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

### Ничего

## НАПРЯЖЕНИЕ

### DeviceJobDetails
Этот командлет получает сведения о **DeviceJob** , который завершается этим командлетом.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


