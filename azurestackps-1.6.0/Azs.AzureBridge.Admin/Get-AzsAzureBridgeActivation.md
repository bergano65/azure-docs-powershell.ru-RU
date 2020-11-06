---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "93570528"
---
# Get-AzsAzureBridgeActivation

## КРАТКИй обзор
Возвращает активацию моста Azure.

## Максимальное

### Список (по умолчанию)
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Получить
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### ResourceId
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## NОПИСАНИЕ
После регистрации стека Azure объект активации содержит данные, которые связывают развертывание стека Azure с его регистрацией в Azure, например Дата окончания срока действия, имя и т. д.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

Получение списка активаций моста Azure в группе ресурсов "activationRG"

### --------------------------ПРИМЕР 2--------------------------
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

Получение активации моста Azure по имени "myActivation", расположенному в разделе "activationRG"

## ПАРАМЕТРЫ

### -Name (имя)
Имя активации.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов, используемая во время регистрации стека Azure; Вы также можете просматривать имена групп ресурсов на портале.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Пропуск первых N элементов, указанных в значении параметра.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Возвращает первые N элементов, заданные значением параметра.
Действует после параметра-Skip.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

