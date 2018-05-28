---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
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