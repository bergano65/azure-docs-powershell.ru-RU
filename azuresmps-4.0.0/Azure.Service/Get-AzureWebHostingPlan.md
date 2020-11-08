---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076512"
---
# Get-AzureWebHostingPlan

## КРАТКИй обзор
Возвращает планы для веб-хостинга Azure в текущей подписке.

## Максимальное

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Get-AzureWebHostingPlan** получает планы веб-хостинга Azure в текущей подписке.

По умолчанию **Get-AzureWebHostingPlan** получает все планы размещения Azure в текущей подписке и возвращает объект, который предоставляет базовые сведения о планах.
При использовании параметров *Space* и *Name* функция **Get-AzureWebHostingPlan** Возвращает определенный объект плана размещения.

Чтобы найти текущую подписку, используйте *текущий* параметр командлета **Get-AzureSubscription** .
Чтобы изменить текущую подписку, используйте командлет **SELECT-AzureSubscription** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех планов размещения веб-сайтов в подписке
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Эта команда получает все планы размещения веб-сайтов Azure в текущей подписке.

### Пример 2: получение определенного плана размещения на веб-сайте в подписке
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Эта команда получает план размещения веб-сайта с именем Default0 в пространстве имен westeuropewebspace в текущей подписке.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя плана в подписке.
По умолчанию этот командлет получает все планы в текущей подписке.
Этот параметр не поддерживает подстановочные знаки.

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

### -WebSpaceName
Указывает имя веб-пространства в подписке.
По умолчанию этот командлет получает все сайты в указанном веб-пространстве.
Этот параметр не поддерживает подстановочные знаки.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
Вы можете передать входные данные этому командлету по имени свойства, но не по значению.

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. WebHostingPlan
По умолчанию **Get-AzureWebHostingPlan** возвращает массив объектов **WebHostingPlan** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

