---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075819"
---
# Set-AzureServiceProject

## КРАТКИй обзор
Настройка расположения по умолчанию, подписки, слота и учетной записи хранения для текущей службы.

## Максимальное

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureServiceProject** задает расположение для развертывания, слот, учетную запись хранения и подписку на текущую службу.
Эти значения используются при публикации службы в облаке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: основные параметры
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Задает расположение для развертывания службы в регионе "Северный центр США".
Задает в качестве слота развертывания производственную среду. Задает учетную запись хранения, которая будет использоваться для размещения определения службы в myStorageAccount.
Задает подписку, на которой будет размещаться служба в mySubscription.
Каждый раз, когда служба публикуется в облаке, она будет размещена в центре обработки данных в регионе Северный Central США, она обновит слот развертывания и будет использовать указанную подписку и учетную запись хранения.

## ПАРАМЕТРЫ

### -Location
Область, в которой будет размещена служба.
Это значение используется при публикации службы в облаке.
Возможны следующие значения: везде, где бы вы ни находились, где бы вы ни находились, Восточной Азии, восток США, Северный Центральная США, Южная Европа, Юго-Восточная часть США, Юго-ru.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Указывает на то, что этот командлет возвращает объект, представляющий элемент, на котором оно работает.
По умолчанию этот командлет не создает никаких выходных данных.

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

### -Slot
Слот (производственный или промежуточный), в котором будет размещена служба.
Это значение используется при публикации службы в облаке.
Возможные значения: "производство", "промежуточный".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Хранилище
Учетная запись хранения, которая будет использоваться при загрузке пакета службы в облако.
Если учетная запись хранения не существует, она будет создана при публикации службы в облаке.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
* node-dev, PHP-Dev, Python-dev

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Publish-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


