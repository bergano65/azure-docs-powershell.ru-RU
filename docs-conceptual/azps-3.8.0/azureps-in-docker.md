---
title: Использование Azure PowerShell в Docker
description: Использование предустановки Azure PowerShell в образе Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740598"
---
# <a name="using-azure-powershell-in-docker"></a>Использование Azure PowerShell в Docker

Мы публикуем образы Docker с предустановкой Azure PowerShell. В этой статье показано, как приступить к работе с Azure PowerShell в контейнере Docker.

## <a name="finding-available-images"></a>Поиск доступных образов

Для выпущенных образов требуется Docker 17.05 или более поздней версии. Также предполагается, что Docker можно запускать без `sudo` или прав локального администратора. Чтобы правильно установить `docker`, следуйте официальным [инструкциям][install] Docker.

Последняя версия образа контейнера содержит последнюю версию PowerShell и последние версии модулей Azure PowerShell, поддерживаемые модулем Az.

Вместе с каждым новым выпуском модуля Az мы выпускаем образ для приведенных ниже операционных систем.

- Ubuntu 18.04 (по умолчанию)
- Debian 9
- CentOS 7

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

Для узлов Windows Docker нужно включить общий доступ к файлам Docker, чтобы предоставить контейнерам Linux общий доступ к локальным диски в Windows. Дополнительные сведения см. в статье [Начало работы с Docker для Windows][file-sharing].

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
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
