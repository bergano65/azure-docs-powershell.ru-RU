---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075870"
---
# Remove-AzureAccount

## КРАТКИй обзор
Удаление учетной записи Azure из Windows PowerShell.

## Максимальное

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureAccount** удаляет учетную запись Azure и ее подписки из файла данных подписки в перемещаемом профиле пользователя.
Эта учетная запись не удаляется из Microsoft Azure, а сама учетная запись может быть изменена любым способом.

Использование этого командлета очень похоже на выход из учетной записи Azure.
Кроме того, если вы хотите снова войти в учетную запись, используйте **Add-AzureAccount** или **Import-AzurePublishSettingsFile** , чтобы снова добавить учетную запись в Windows PowerShell.

Вы также можете использовать командлет **Remove-AzureAccount** , чтобы изменить способ входа командлетов PowerShell для Azure в учетную запись Azure.
Если у вашей учетной записи есть сертификат управления из **Import-AzurePublishSettingsFile** и маркер доступа из **Add-AzureAccount** , командлеты PowerShell для Azure используют только маркер доступа. они игнорируют сертификат управления.
Чтобы использовать сертификат управления, выполните **Remove-AzureAccount**.
Когда **Remove-AzureAccount** находит как сертификат управления, так и маркер доступа, он удаляет только маркер доступа, а не удаляет учетную запись.
Сертификат управления по-прежнему есть, поэтому учетная запись по-прежнему доступна для Windows PowerShell.

В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление учетной записи
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Эта команда удаляет admin@contoso.com из файла данных подписки.
После завершения команды учетная запись больше не доступна для Windows PowerShell.

## ПАРАМЕТРЫ

### -Force
Подавляет вывод запроса подтверждения.
По умолчанию **Remove-AzureAccount** предложит вам перед удалением учетной записи из Windows PowerShell.

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

### -Name (имя)
Указывает имя учетной записи, которую нужно удалить.
Значение параметра задается с учетом регистра.
Подстановочные знаки не поддерживаются.

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
Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.
По умолчанию этот командлет не возвращает никаких выходных данных.

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

### Ничего
Вы можете передавать входные данные командлету по имени свойства, но не по значению.

## НАПРЯЖЕНИЕ

### None и System. Boolean
Если вы используете параметр *PassThru* , этот командлет возвращает логическое значение.
В противном случае он не возвращает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


