---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077412"
---
# Remove-WAPackStaticIPAddressPool

## КРАТКИй обзор
Удаляет объекты пула статических IP-адресов.

## Максимальное

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Эти разделы устарели и будут исключены в будущем.
В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.
Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Remove-WAPackStaticIPAddressPool** удаляет статические объекты пула IP-адресов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление статического пула IP-адресов
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

Первая команда получает пул статических IP-адресов с именем ContosoStaticIPAddressPool01 с помощью командлета **Get-WAPackStaticIPAddressPool** , а затем сохраняет этот объект в переменной $StaticIPAddressPool.

Вторая команда удаляет пул статических IP-адресов, хранящийся в $StaticIPAddressPool.
В командной строке появится запрос на подтверждение.

### Пример 2: Удаление статического пула IP-адресов без подтверждения
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

Первая команда получает статический пул IP-адресов с именем ContosoStaticIPAddressPool02 с помощью командлета **Get-WAPackStaticIPAddressPool** , а затем сохраняет этот объект в переменной $ StaticIPAddressPool.

Вторая команда удаляет пул статических IP-адресов, хранящийся в $StaticIPAddressPool.
Эта команда включает параметр *Force* .
Команда не запрашивает подтверждение.

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

### -PassThru
Возвращает объект, который представляет собой элемент, с которым вы работаете.
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

### -StaticIPAddressPool
Указывает StaticIPAddressPool.
Для получения пула статических IP-адресов используйте командлет **Get-WAPackStaticIPAddressPool** .

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-WAPackStaticIPAddressPool](./Get-WAPackStaticIPAddressPool.md)

[Remove-WAPackStaticIPAddressPool](./Remove-WAPackStaticIPAddressPool.md)


