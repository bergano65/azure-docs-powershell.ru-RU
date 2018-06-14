---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853021"
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