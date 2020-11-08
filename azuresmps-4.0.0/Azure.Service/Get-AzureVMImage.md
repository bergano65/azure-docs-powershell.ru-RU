---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076532"
---
# Get-AzureVMImage

## КРАТКИй обзор
Получает свойства одного или списка операционных систем или образа виртуальной машины в репозитории изображений.

## Максимальное

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureVMImage** получает свойства одного или списка операционных систем или образа виртуальной машины в репозитории изображений.
Командлет возвращает сведения обо всех изображениях в репозитории или об определенном изображении, если оно указано.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение определенного объекта изображения из текущего репозитория изображений.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Эта команда получает объект Image с именем Image001 из текущего репозитория изображений.

### Пример 2: получение всех изображений из текущего репозитория изображений
```
PS C:\> Get-AzureVMImage
```

Эта команда извлекает все изображения из текущего репозитория изображений.

### Пример 3: Настройка контекста подписки, а затем получение всех изображений
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Эта команда задает контекст подписки, а затем извлекает все изображения из репозитория изображений.

## ПАРАМЕТРЫ

### -ImageName
Указывает имя операционной системы или образа виртуальной машины в репозитории изображений.
Если этот параметр не указан, возвращаются все изображения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Сохранить — AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


