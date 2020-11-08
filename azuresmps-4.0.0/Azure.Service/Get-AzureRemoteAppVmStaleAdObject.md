---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075630"
---
# Get-AzureRemoteAppVmStaleAdObject

## КРАТКИй обзор
Возвращает объекты в службе Azure Active Directory, связанные с виртуальными машинами RemoteApp Azure, которые больше не существуют.

## Максимальное

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRemoteAppVmStaleAdObject** получает объекты в службе Azure Active Directory, связанные с виртуальными машинами RemoteApp Azure, которые больше не существуют.
Этот командлет выводит имя каждого объекта, который он получает.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение устаревших объектов для коллекции
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

Эта вторая команда получает старые объекты для коллекции с именем Contoso.

## ПАРАМЕТРЫ

### -CollectionName
Указывает имя коллекции Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Указывает учетные данные с правами на выполнение этого действия.
Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .
Если этот параметр не указан, этот командлет использует учетные данные текущего пользователя.

```yaml
Type: PSCredential
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Подстрок

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Clear-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


