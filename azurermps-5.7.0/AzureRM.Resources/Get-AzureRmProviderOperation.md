---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734008"
---
# Get-AzureRmProviderOperation

## КРАТКИй обзор
Возвращает операции для поставщика ресурсов Azure, защищаемые с помощью Azure RBAC.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Get-AzureRmProviderOperation получает операции, предоставляемые поставщиками ресурсов Azure.
Операции могут составляться для создания настраиваемых ролей в Azure RBAC.
Команда принимает в качестве входных данных строку поиска (с возможными подстановочными знаками (*)), которая определяет отображаемые сведения об операциях.

Используйте Get-AzureRmProviderOperation * для получения всех операций для всех поставщиков ресурсов Azure.

Используйте Get-AzureRmProviderOperation Microsoft. COMPUTE/* для получения всех операций поставщика Microsoft. COMPUTE Resource.

## ИЛЛЮСТРИРУЮТ

### Получение всех действий для всех поставщиков
```
PS C:\> Get-AzureRmProviderOperation *
```

### Получение действий для определенного поставщика ресурсов
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### Получение всех действий, которые можно выполнять на виртуальных машинах
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
Строка поиска операции (с возможными подстановочными знаками (*))

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Подстрок
Параметр "OperationSearchString" принимает значение типа String из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Resources. PSResourceProviderOperation

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
