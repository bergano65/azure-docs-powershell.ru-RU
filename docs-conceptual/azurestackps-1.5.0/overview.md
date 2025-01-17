---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56154229"
---
# <a name="azure-stack-module-150"></a>Модуль Azure Stack версии 1.5.0

## <a name="requirements"></a>Требования:
Минимальная поддерживаемая версия Azure Stack — 1808.

Примечание. Если вы используете более раннюю версию, установите версию 1.4.0.

## <a name="known-issues"></a>Известные проблемы:

- New-AzsOffer не позволяет создать общедоступное предложение. После него нужно вызвать командлет Set-AzsOffer, чтобы изменить состояние.
- Нельзя удалить пул IP-адресов без повторного развертывания.

## <a name="install"></a>Install
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>Заметки о выпуске
* Все модули администрирования Azure Stack обновлены и зависят от модуля AzureRm.Profile такой же или более поздней версии.
* Добавлена поддержка обработки имен вложенных ресурсов во всех модулях.
* Исправление ошибки во всех модулях, когда параметру ErrorActionPreference принудительно присваивалось значение Stop.
* Модуль Azs.Compute.Admin
    * Добавлены новые свойства квот для поддержки управляемых дисков.
    * Добавлены командлеты для переноса дисков.
    * Дополнительные свойства для объектов образа платформы и расширений виртуальных машин.
* Azs.Fabric.Admin 
    * Новый командлет для добавления узла единицы масштабирования.
* Azs.Backup.Admin
    * Set-AzsBackupShare — это псевдоним командлета Set-AzsBackupConfiguration.
    * Get-AzsBackupLocation — это псевдоним командлета Get-AzsBackupConfiguration
    * В Set-AzsBackupConfiguration параметр BackupShare — это псевдоним для параметра path.
* Azs.Subscriptions
    * В Get-AzsDelegatedProviderOffer параметр OfferName — это псевдоним для Offer.
* Azs.Subscriptions.Admin
    * В Get-AzsDelegatedProviderOffer параметр OfferName — это псевдоним для Offer.

## <a name="content"></a>Содержимое:
### <a name="azure-bridge"></a>Мост Azure
Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.

### <a name="backup"></a>Azure Backup
Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:
- настраивать расположение для хранения резервных копий;
- выполнять резервное копирование;
- выводить список созданных резервных копий и выполнять на их основе восстановление.

### <a name="commerce"></a>Приложения для коммерции
Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.

### <a name="compute"></a>Службы вычислений
Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ, управляемыми дисками и расширениями виртуальных машин.

### <a name="fabric"></a>Fabric
Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:
- остановка, запуск и завершение работы для узлов единиц масштабирования;
- очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;
- исправление узлов единиц масштабирования;
- перезапуск роли инфраструктуры;
- остановка, запуск и завершение работы экземпляров роли инфраструктуры;
- создание пулов IP-адресов.


### <a name="gallery"></a>Коллекция
Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:
- просматривать сведения о работоспособности ресурсов отметок в Azure Stack;
- просматривать оповещения и управлять ими.

### <a name="keyvault"></a>Хранилище ключей
Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.

### <a name="network"></a>Сеть
Предварительная версия модуля для администраторов сетей, которая позволяет:
- управлять квотами сети;
- просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;
- использовать командлет для отображения общих сведений об администраторе.

### <a name="storage"></a>Хранилище
Предварительная версия модуля для администраторов хранилища Azure Stack.  В этом выпуске мы предоставляем следующие функции:
- управление квотами хранилища;
- сборка мусора для удаленных ресурсов хранилища;
- восстановление удаленных учетных записей хранения;
- перенос контейнеров из одной общей папки в другую;
- просмотр сведений об отдельных компонентах хранилища;
- просмотр сведений об использовании и производительности.

### <a name="subscription-admin"></a>Администратор подписки
Предварительная версия модуля для администраторов подписки Azure Stack.  Этот модуль предоставляет следующие функции для администраторов:
- управление планами и предложениями;
- просмотр сведений об использовании и производительности.
- Управление RBAC

### <a name="subscription"></a>Подписка
Предварительная версия модуля подписки Azure Stack.  Этот модуль предоставляет следующие функции для пользователей:
- создание, удаление и изменение подписок.

### <a name="update"></a>Блокировка изменений
Предварительная версия модуля для администраторов обновлений Azure Stack.  В этом модуле администраторы могут:
- выводить список и устанавливать доступные обновления;
- возобновлять прерванную установку обновлений;
- просматривать установленные обновления.
