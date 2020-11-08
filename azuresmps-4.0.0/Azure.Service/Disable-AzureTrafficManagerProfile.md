---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075693"
---
# Disable-AzureTrafficManagerProfile

## КРАТКИй обзор
Отключение профиля диспетчера трафика.

## Максимальное

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Disable-AzureTrafficManagerProfile** отключает профиль диспетчера трафика Microsoft Azure.
Вы можете использовать параметр *PassThru* , чтобы показать, выполняется ли операция успешно.

## ИЛЛЮСТРИРУЮТ

### Пример 1: отключение профиля диспетчера трафика и отображение результатов
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Эта команда отключает профиль диспетчера трафика с именем отобразите.
Команда определяет параметр *PassThru* , чтобы показать, успешно ли команда выполнена.

### Пример 2: отключение профиля диспетчера трафика и отображение результатов
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Эта команда отключает профиль диспетчера трафика с именем отобразите, но не показывает, была ли команда выполнена успешно.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя профиля диспетчера трафика, который нужно отключить.

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

### -PassThru
Возвращает $True, если операция выполнена успешно. в противном случае $False.
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
Указывает профиль Azure, из которого считывается этот командлет. Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### System. Boolean
Этот командлет создает $True или $False.
Если операция выполнена успешно и вы указываете параметр *PassThru* , этот командлет возвращает значение $true.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


