---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731776"
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

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Общие сведения об администраторе сети.

### --------------------------ПРИМЕР 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Получение сведений об использовании общедоступного IP-адреса.

## ПАРАМЕТРЫ

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

