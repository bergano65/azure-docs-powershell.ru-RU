---
title: "Журнал изменений Azure PowerShell | Документация Майкрософт"
description: "Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2017
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="version-129"></a>Версия 1.2.9

Изменения в этом выпуске

* Модуль AzureRm.AzureStackAdmin
    + Изменения в командлете Add-AzureRmResourceProviderRegistration для поддержки разделения Azure Resource Manager для администратора и для клиента. Добавлен новый параметр -ResourceManagerType.
    + Удалены параметры -AdminUri, -ApiVersion, -SubscriptionId и -Token из каждого командлета. Мы предупреждали о том, что поддержка этих параметров будет прекращена, и теперь они удалены.
* Модуль AzureStackStorage
    + Добавлены новые командлеты для поддержки сценариев миграции контейнера.
    + Удалены командлеты, ссылающиеся на внутренние компоненты и базовые функции.
* AzureRM.BootStrapper
    + Создан модуль для управления версиями командлетов Azure PowerShell с помощью профилей версии.