---
title: Перенос скриптов Azure PowerShell с AzureRM на Az
description: Сведения о действиях и инструментах для переноса скриптов с модуля AzureRM на новый модуль Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021097"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Перенос Azure PowerShell с AzureRM на Az

Все версии модуля AzureRM PowerShell устарели, но все еще поддерживаются. [Модуль Az PowerShell](install-az-ps.md) теперь является рекомендуемым модулем PowerShell для взаимодействия с Azure.

Скрипты, написанные для командлетов AzureRM, не смогут автоматически работать с новым модулем. Чтобы упростить этот переход, был разработан [набор средств для миграции с AzureRM на Az](https://github.com/Azure/azure-powershell-migration). Миграция всегда сопряжена со сложностями, и эта статья поможет вам начать переход на новый модуль Az PowerShell. Дополнительные сведения о том, для чего был создан модуль Az PowerShell, см. в статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md).

Полный список критических изменений между AzureRM и Az см. [здесь](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Убедитесь, что существующие скрипты работают с последним выпуском AzureRM

Перед выполнением любых действий миграции проверьте, какие версии AzureRM установлены в вашей системе.
Это позволит проверить, запущены ли скрипты с последним выпуском, и поможет узнать, какие версии AzureRM необходимо удалить.

Чтобы проверить установленные версии AzureRM, выполните приведенный ниже пример.

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

**Последний** доступный выпуск AzureRM — **6.13.1**. Если у вас нет этой версии, возможно, ваши существующие скрипты нужно будет изменить для работы с модулем Az в дополнение к изменениям, описанным в этой статье и [списке критических изменений](migrate-az-1.0.0.md).

Если скрипты не работают с AzureRM 6.13.1, обновите их в соответствии с [руководством по переходу AzureRM с версии 5.x на 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Если вы используете более раннюю версию модуля AzureRM, найдите нужное руководство. Руководства по миграции существуют для каждого основного номера версии.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Установка набора средств для миграции с AzureRM на Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>Автоматический перенос скриптов PowerShell

Используя набор средств для миграции с AzureRM на Az, вы можете подготовить план, который определяет изменения, которые будут внесены в скрипты до их внесения и установки модуля Az PowerShell.

В статье [Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) показано, как выполнить автоматический перенос скриптов PowerShell из AzureRM в модуль Az PowerShell.

## <a name="next-steps"></a>Дальнейшие действия

[Установка Azure PowerShell](install-az-ps.md)
[Удаление AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
