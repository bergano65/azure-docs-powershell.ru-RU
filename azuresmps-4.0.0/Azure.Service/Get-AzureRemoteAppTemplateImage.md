---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076579"
---
# Get-AzureRemoteAppTemplateImage

## КРАТКИй обзор
Получение сведений об изображениях шаблонов Azure RemoteApp.

## Максимальное

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRemoteAppTemplateImage** извлекает сведения об изображениях шаблонов Azure RemoteApp в Microsoft Azure.
Этот командлет возвращает объект, содержащий сведения об указанном изображении шаблона.
Если вы не указали изображение шаблона, оно извлекает сведения обо всех его изображениях в текущей подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение списка всех изображений шаблонов
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Эта команда возвращает список всех изображений шаблонов.

### Пример 2: получение сведений об указанном образе шаблона
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Эта команда извлекает сведения об изображении шаблона с именем ContosoApps.

## ПАРАМЕТРЫ

### -ImageName
Указывает имя образа шаблона Azure RemoteApp.

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

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


