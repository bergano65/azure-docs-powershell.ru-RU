---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076570"
---
# Get-AzureRemoteAppVNet

## КРАТКИй обзор
Получение сведений о виртуальных сетях RemoteApp Azure в Azure.

## Максимальное

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRemoteAppVNet** извлекает сведения о виртуальных сетях Azure RemoteApp в Microsoft Azure.
Этот командлет возвращает объект, содержащий сведения об указанной виртуальной сети.
Если виртуальная сеть не указана, этот командлет возвращает сведения обо всех виртуальных сетях в текущей подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений о виртуальной сети
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Эта команда получает сведения о виртуальной сети с именем ContosoVNet.

## ПАРАМЕТРЫ

### -IncludeSharedKey
Указывает на то, что этот командлет включает значение общего ключа в извлеченных данных о виртуальной сети.

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

### -VNetName
Указывает имя виртуальной сети RemoteApp Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


