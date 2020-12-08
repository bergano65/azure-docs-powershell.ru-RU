---
title: Знакомство с модулем Azure Az PowerShell
description: Знакомство с модулем Az PowerShell, рекомендуемым для взаимодействия с Azure вместо модуля AzureRM PowerShell.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: d922affd608ebfce41f9608ec82d565d6afe9f7f
ms.sourcegitcommit: 3ef9f7f6c20af98282a0499b1527c291ee54011b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "96617725"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Знакомство с модулем Azure Az PowerShell

## <a name="overview"></a>Обзор

Модуль Az PowerShell — это набор командлетов для управления ресурсами Azure непосредственно из PowerShell. PowerShell предоставляет мощные возможности автоматизации, которые можно использовать для управления ресурсами Azure, например, в контексте конвейера CI/CD.

Модуль Az PowerShell является заменой AzureRM. Теперь это рекомендуемая версия для взаимодействия с Azure.

Модуль Az PowerShell можно использовать с одним из следующих методов:

* [установив модуль Az PowerShell с помощью PowerShellGet](install-az-ps.md) (рекомендуемый вариант);
* [установив модуль Az PowerShell с помощью MSI;](install-az-ps-msi.md)
* [используя Azure Cloud Shell;](/azure/cloud-shell/overview)
* [используя контейнер Docker Az PowerShell.](azureps-in-docker.md)

## <a name="features"></a>Компоненты

Использование модуля Az PowerShell связано с рядом преимуществ.

* Безопасность и стабильность:
  * шифрование кэша токенов;
  * поддержка ADFS 2019;
  * механизм безопасности, позволяющий предотвратить атаки типа "злоумышленник в середине";
  * поддержка таких функций, как Непрерывная оценка доступа (будет реализована в 2021 г.).
* Поддержка всех служб Azure:
  * модуль доступен для каждой службы Azure;
  * исправление ряда ошибок и обновление версий API, используемых с AzureRM.
* Несколько дополнительных новых возможностей:
  * поддержка в Cloud Shell и кросс-платформенных решениях;
  * возможность получения и использования маркера доступа для доступа к ресурсам Azure;
  * универсальный командлет Az для операций типа штриховки с escape-символами.

> [!NOTE]
> Для работы в Az PowerShell на всех платформах мы рекомендуем использовать PowerShell версии 7.x и выше.

Модуль Az PowerShell основан на библиотеке .NET Standard и работает с PowerShell 7 и более поздних версий на всех платформах, включая Windows, macOS и Linux. Он также совместим с Windows PowerShell 5.1.

Мы стремимся обеспечить поддержку Azure на всех платформах, поэтому модули Az PowerShell являются кросс-платформенными.

## <a name="upgrade-your-environment-to-az"></a>Обновление среды до Az

Для включения поддержки новых функций Azure в PowerShell необходимо перейти на модуль Az. Если вы не готовы установить модуль Az в качестве замены AzureRM, вам доступны несколько способов экспериментирования с Az.

* Использование среды `PowerShell` с [Azure Cloud Shell](/azure/cloud-shell/overview). Azure Cloud Shell — это браузерная среда оболочки, которая поставляется с пакетом установки модуля Az и поддерживает псевдонимы совместимости `Enable-AzureRM`.
* Не удаляйте модуль AzureRM, установленный в Windows PowerShell 5.1. Просто установите модуль Az в PowerShell версии 7 или выше. Windows PowerShell 5.1 и PowerShell версии 7 или выше используют разные коллекции модулей. Выполните инструкции по установке [последней версии PowerShell](/powershell/scripting/install/installing-powershell), а затем [установите модуль Az](install-az-ps.md) из PowerShell версии 7 или выше.

Чтобы выполнить обновление из существующей установки AzureRM, сделайте следующее:

1. [Удалите модуль AzureRM для Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
1. [Установите модуль Az для Azure PowerShell](install-az-ps.md).
1. **НЕОБЯЗАТЕЛЬНО**. Активируйте режим совместимости, чтобы добавить псевдонимы для командлетов AzureRM с помощью [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias), пока вы не ознакомитесь с новым набором команд. Дополнительные сведения см. в следующем разделе или в статье [Перенос Azure PowerShell с AzureRM на Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Перенос существующих скриптов с AzureRM на Az

Если ваши скрипты зависят от модуля AzureRM, вы можете выполнить перенос с помощью нескольких ресурсов:

* [Перенос Azure PowerShell с AzureRM на Az](migrate-from-azurerm-to-az.md)
* [Полный список критических изменений между AzureRM и Az 1.0.0](migrate-az-1.0.0.md)
* Командлет [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

## <a name="supportability"></a>Возможности поддержки

Az — это актуальный модуль PowerShell для Azure. Проблемы или запросы функций можно регистрировать непосредственно в [репозитории GitHub](https://github.com/Azure/azure-powershell) или через службу поддержки Майкрософт, если у вас есть контракт на поддержку. Возможность запроса функций будет реализована в последней версии Az. Функция критических проблем будет реализована в двух последних версиях Az.

В AzureRM больше не будут добавляться новые командлеты или функции. Но модуль AzureRM по-прежнему официально поддерживается. Критические ошибки в нем будут исправляться по февраль 2021 года.

## <a name="data-collection"></a>сбор данных

Azure PowerShell собирает данные телеметрии по умолчанию. Корпорация Майкрософт агрегирует собранные данные для определения закономерностей использования, обнаружения распространенных проблем и улучшения работы Azure PowerShell.
Microsoft Azure PowerShell не собирает личные или персональные данные. Например, данные об использовании позволяют определить проблемы, вызванные, например, командлетами с низким процентом выполнений, и помогают задать приоритеты для нашей работы.

Хотя для нас важно получать эти ценные сведения, мы также понимаем, что не все хотят передавать данные об использовании. Сбор данных можно отключить с помощью командлета [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection). Вы также можете ознакомиться с нашим [заявлением о конфиденциальности](https://privacy.microsoft.com/privacystatement), чтобы получить дополнительные сведения.
