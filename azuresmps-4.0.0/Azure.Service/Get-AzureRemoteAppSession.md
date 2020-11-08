---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076577"
---
# Get-AzureRemoteAppSession

## КРАТКИй обзор
Список всех активных и отключенных сеансов удаленных приложений Azure для коллекции.

## Максимальное

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRemoteAppSession** перечисляет все активные и отключенные сеансы удаленных приложений Azure для коллекции Azure RemoteApp.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех сеансов в коллекции
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

Эта команда перечисляет все сеансы в коллекции Azure RemoteApp с именем ContosoApps.

## ПАРАМЕТРЫ

### -CollectionName
Указывает имя коллекции Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### -UserUpn
Указывает имя участника-пользователя (UPN) пользователя, для которого требуется получить сеансы RemoteApp Azure.
Например, имя участника-пользователя может быть представлено в следующем формате: PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Разъединить — AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Invoke-AzureRemoteAppSessionLogoff](./Invoke-AzureRemoteAppSessionLogoff.md)

[Send-AzureRemoteAppSessionMessage](./Send-AzureRemoteAppSessionMessage.md)


