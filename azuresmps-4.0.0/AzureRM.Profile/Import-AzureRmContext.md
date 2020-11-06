---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554915"
---
# Import-AzureRmContext

## КРАТКИй обзор
Загрузка данных проверки подлинности Azure из файла.

## Максимальное

### InMemoryProfile
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### ProfileFromDisk
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## NОПИСАНИЕ
Командлет Import-AzureRmContext загружает данные для проверки подлинности из файла, чтобы установить среду и контекст Azure.
Командлеты, выполняемые в текущем сеансе, используют эти сведения для проверки подлинности запросов в диспетчере ресурсов Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: импорт контекста из AzureRmProfile
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

В этом примере выполняется импорт контекста из PSAzureProfile, который передается в командлет.

### Пример 2: импорт контекста из JSON-файла
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

В этом примере выделяется контекст из JSON-файла, который передается в командлет.
Этот JSON-файл можно создать из импорта — AzureRmContext.

## ПАРАМЕТРЫ

### -AzureContext
Указывает контекст Azure, из которого считывается этот командлет.
Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Указывает путь к контекстной информации, сохраненной с помощью команды Save-AzureRMContext.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile
System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Profile. Models. PSAzureProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

