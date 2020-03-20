---
title: Использование Azure PowerShell в Docker
description: Использование предустановки Azure PowerShell в образе Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402686"
---
# <a name="using-azure-powershell-in-docker"></a>Использование Azure PowerShell в Docker

Мы публикуем образы Docker с предустановкой Azure PowerShell. В этой статье показано, как приступить к работе с Azure PowerShell в контейнере Docker.

## <a name="finding-available-images"></a>Поиск доступных образов

Для выпущенных образов требуется Docker 17.05 или более поздней версии. Также предполагается, что Docker можно запускать без `sudo` или прав локального администратора. Чтобы правильно установить `docker`, следуйте официальным [инструкциям][install] Docker.

Выпущенные контейнеры создаются на основе официальных контейнеров PowerShell, к которым затем в качестве определенного уровня добавляется модуль Az.

Последний стабильный образ включает следующие компоненты:

- Ubuntu 18.04
- PowerShell версии 6.2.4
- Актуальный модуль Az Azure PowerShell

См. [полный список доступных образов Docker][az image].

## <a name="using-azure-powershell-in-a-container"></a>Использование Azure PowerShell в контейнере

Ниже представлены команды Docker, необходимые для скачивания образа и запуска интерактивного сеанса PowerShell.

1. Скачайте последнюю версию образа azure-powershell.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Запустите контейнер azure-powershell в интерактивном режиме:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Запуск контейнера azure-powershell в интерактивном режиме с использованием проверки подлинности узла

Если в системе с Docker есть установка Azure PowerShell, возможно, доступны кэшированные учетные данные Azure. Эти учетные данные можно использовать в сеансе PowerShell, выполняющемся в контейнере Docker.

По умолчанию кэшированные учетные данные находятся в каталоге `$HOME/.Azure` на узле. Служба Docker должна иметь доступ к этому расположению для получения доступа к учетным данным. Следующая команда запускает контейнер с подключенным кэшем учетных данных, а также интерактивный сеанс PowerShell.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Удаление ненужного образа

Приведенная ниже команда служит для удаления контейнера Docker, если он больше не нужен.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell