---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075703"
---
# Clear-AzureRemoteAppVmStaleAdObject

## КРАТКИй обзор
Удаление объектов из Azure Active Directory, связанных с виртуальными машинами RemoteApp Azure, которые больше не существуют.

## Максимальное

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **clear-AzureRemoteAppVmStaleAdObject** удаляет объекты в службе Azure Active Directory, связанные с виртуальными машинами RemoteApp Azure, которые больше не существуют.
Для удаления объектов Azure Active Directory необходимо использовать учетные данные, имеющие права.
Если вы задаете *подробный* общий параметр, этот командлет выводит имя каждого объекта, который он удаляет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление устаревших объектов для коллекции
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

Первая команда запрашивает имя пользователя и пароль с помощью команды **Get-Credential**.
Команда сохраняет результаты в переменной $AdminCredentials.

Вторая команда очищает устаревшие объекты для коллекции с именем Contoso.
В команде используются учетные данные, хранящиеся в переменной $AdminCredentials.
Для успешного завершения команды эти учетные данные должны иметь соответствующие права.

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

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


