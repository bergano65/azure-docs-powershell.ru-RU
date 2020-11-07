---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909078"
---
# Get-AzsNetworkAdminOverview

## КРАТКИй обзор
Получите общие сведения о состоянии поставщика сетевых ресурсов.

## Максимальное

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## NОПИСАНИЕ
Получите общие сведения о состоянии поставщика сетевых ресурсов. Отдельные свойства предоставляют подробные сведения об использовании ресурсов и работоспособности компонента.

## ИЛЛЮСТРИРУЮТ

### ПРИМЕР 1
```
Get-AzsNetworkAdminOverview
```

Общие сведения об администраторе сети.

### ПРИМЕР 2
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Получение сведений об использовании общедоступного IP-адреса.

## ПАРАМЕТРЫ

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
