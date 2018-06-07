---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819717"
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