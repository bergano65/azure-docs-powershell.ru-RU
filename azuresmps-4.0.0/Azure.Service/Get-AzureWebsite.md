---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0eb3f56ff4c14d19493531367c9b29286b8c560
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104718228"
---
# Get-AzureWebsite

## SYNOPSIS
Получает веб-сайты Azure в текущей подписке.

## СИНТАКСИС

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его использованием можно получить сведения** о веб-сайтах Azure в текущей подписке.

По умолчанию **get-AzureWebsite** получает все веб-сайты Azure в текущей подписке и возвращает объект, который предоставляет основные сведения о сайтах.
При использовании параметра *Name* **get-AzureWebsite** возвращает объект с большой информацией, включая сведения о конфигурации.

Текущая подписка — это подписка, которая обозначена как "текущая". Чтобы найти текущую подписку, используйте параметр *Current* для cmdlet [Get-AzureSubscription.](/powershell/module/servicemanagement/azure.service/get-azuresubscription)
Чтобы изменить текущую подписку, используйте [cmdlet Select-AzureSubscription.](/powershell/module/servicemanagement/azure.service/select-azuresubscription)

В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .

## ПРИМЕРЫ

### Пример 1. Получить все веб-сайты в подписке
```
PS C:\> Get-AzureWebsite
```

Эта команда получает все веб-сайты Azure в текущей подписке.

### Пример 2. Получить веб-сайт по имени
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Эта команда получает подробные сведения о веб-сайте ContosoWeb Azure, включая сведения о конфигурации.
При использовании параметра *Name* **get-AzureWebsite** возвращает объект **SiteWithConfig** с расширенными сведениями о веб-сайте.

### Пример 3. Подробные сведения обо всех веб-сайтах
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Эта команда получает подробные сведения обо всех веб-сайтах в подписке.
Она использует команду **Get-AzureWebsite** для получения всех веб-сайтов, а затем использует командлет **ForEach-Object** для получения каждого веб-сайта по имени.

### Пример 4. Сведения о слоте развертывания
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Эта команда получает слот для промежуточного развертывания веб-сайта ContosoWeb.
Слоты развертывания можно использовать для тестирования различных версий веб-сайта Azure, не выпуская их для общего использования.

### Пример 5. Получить экземпляры веб-сайтов
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

В этом примере команды используют свойство Instances веб-сайта Azure для получения сведений о текущих экземплярах веб-сайтов.
Свойство **Instances** было добавлено к объекту **SiteWithConfig** в версии 0.8.3 модуля Azure.

Первая команда получает все запущенные экземпляры веб-сайта.
Вторая команда получает количество запущенных экземпляров веб-сайта.
Свойство **"Количество" можно использовать для** любого массива.

## PARAMETERS

### -Name
Подробные сведения о конфигурации указанного веб-сайта.
Введите имя одного из веб-сайтов в подписке.
По умолчанию **get-AzureWebsite** получает все веб-сайты в текущей подписке.
Значение *"Имя"* не поддерживает поддиавные знаки.

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

### -Profile
Определяет профиль Azure, для которого читается этот cmdlet.
Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.

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
Получает указанный слот развертывания веб-сайта.
Введите название слота, например "Промежуточное время" или "Производство".
Дополнительные сведения о слотах для развертывания см. в сведениях о поэтапном развертывании на веб-сайтах Microsoft https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ Azure.
Чтобы добавить слот развертывания на существующий веб-сайт Azure, воспользуйтесь Set-AzureWebsite управления.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet можно ввести по имени свойства, но не по значению.

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site
По умолчанию **get-AzureWebsite** возвращает массив **объектов** сайта.

### Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig
При использовании *параметра Name* **get-AzureWebsite** возвращает объект **SiteWithConfig.**

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Stop-AzureWebsite](./Stop-AzureWebsite.md)

[Show-AzureWebsite](./Show-AzureWebsite.md)


