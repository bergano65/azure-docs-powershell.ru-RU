---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562203"
---
# Find-AzureRmResourceGroup

## КРАТКИй обзор
Поиск групп ресурсов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Find-AzureRmResourceGroup** выполняет поиск групп ресурсов с использованием указанных параметров.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Поиск всех групп ресурсов
```
PS C:\>Find-AzureRmResourceGroup
```

Эта команда находит все группы ресурсов.

### Пример 2: Поиск групп ресурсов по названию тега
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

Эта команда находит все группы ресурсов, у которых есть тег с именем testtag.

### Пример 3: Поиск групп ресурсов по имени и значению тега
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

Эта команда находит все группы ресурсов, у которых есть тег с именем testtag, и значение testval.

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию используемого API поставщика ресурсов. Если вы не укажете версию, этот командлет использует последнюю доступную версию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Тег
Определяет сведения о теге в виде хэш-таблицы, чтобы отфильтровать результаты. Используйте следующие форматы:

@ {tagName = $null} или @ {tagName = ' tagValue '}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### System. Management. Automation. PSObject

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

