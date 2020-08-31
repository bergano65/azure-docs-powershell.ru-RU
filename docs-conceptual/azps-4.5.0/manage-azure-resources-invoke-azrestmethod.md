---
title: Управление ресурсами Azure с помощью командлета Invoke-AzRestMethod
description: Как использовать Azure PowerShell, чтобы управлять ресурсами с помощью командлета Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.openlocfilehash: 6a267e28ec8e2540ce7d6431ffd9aab0b2090c6a
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821369"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Управление ресурсами Azure с помощью командлета Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) — это командлет Azure PowerShell, представленный в модуле PowerShell Az версии 4.4.0. Он позволяет выполнять пользовательские HTTP-запросы к конечной точке управления ресурсами Azure (ARM) с использованием контекста Az.

Этот командлет удобно использовать, если требуется управлять службами Azure для функций, которые еще не доступны в модуле Az PowerShell.

## <a name="how-to-use-invoke-azrestmethod"></a>Как использовать командлет Invoke-AzRestMethod

Например, вы можете разрешить доступ к Реестру контейнеров Azure (ACR) только для конкретных сетей или запретить общий доступ. На момент выхода версии модуля Az PowerShell 4.5.0 эта функция еще не доступна в [модуле PowerShell Az.ContainerRegistry](/powershell/module/Az.ContainerRegistry/). Однако на промежуточном этапе ею можно управлять с помощью `Invoke-AzRestMethod`.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Использование Invoke-AzRestMethod с операциями Get

В следующем примере показано, как использовать командлет `Invoke-AzRestMethod` с операцией Get.

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

Чтобы обеспечить максимальную гибкость, большинство параметров для `Invoke-AzRestMethod` являются необязательными.
Однако при управлении ресурсами в группе ресурсов вам, скорее всего, потребуется указать полный идентификатор ресурса или такие параметры, как группа ресурсов, поставщик ресурсов и тип ресурса.

Параметры `ResourceType` и `Name` могут принимать несколько значений при использовании для ресурсов, требующих более одного имени. Например, параметры для управления сохраненными результатами поиска в рабочей области Log Analytics выглядят как в следующем примере: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

С помощью сопоставления на основе позиции в массиве командлет конструирует следующий ресурс: `Id:'/workspaces/my-la/savedsearches/my-search'`.

Параметр `APIVersion` позволяет использовать определенную версию API, в том числе предварительные версии. Поддерживаемые версии API для поставщиков ресурсов Azure можно найти в репозитории GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).

Определение версии 2019-12-01-preview для ACR можно найти в следующем расположении: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Использование Invoke-AzRestMethod с операциями Patch

Вы можете отключить общий доступ к существующему списку ACR с именем `myacr` в группе ресурсов `myresourcegroup` с помощью командлета `Invoke-AzRestMethod`.

Чтобы отключить общий сетевой доступ, нужно выполнить вызов **PATCH** к API, который изменяет значение параметра `publicNetwokAccess`, как показано в примере ниже.

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

Свойство `Payload` — это строка JSON, содержащая путь к изменяемому свойству.

Все параметры для этого API описаны в связанном с ним файле **rest-api-spec**.
Определение параметра publicNetworkAccess можно найти в [JSON-файле реестра контейнеров](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) для предварительной версии API 2019-12-01.

Чтобы разрешить доступ к реестру только с определенного IP-адреса, необходимо изменить полезные данные, как показано в следующем примере.

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Сравнение с Get-AzResource, New-AzResource и Remove-AzResource

Командлеты `*-AzResource` позволяют настроить вызов REST API к Azure, указав тип ресурса, версию API и обновляемые свойства. Но сначала необходимо создать свойства в виде `PSObject`. Это может заметно усложнить процесс.

`Invoke-AzRestMethod` обеспечивает более простой способ управления ресурсами Azure. Как показано в предыдущем примере, можно создать строку JSON и использовать ее для настройки вызова REST API без предварительного создания `PSObjects`.

Если вам уже знакомы командлеты `*-AzResource`, то вы можете и дальше их использовать. Мы не планируем прекращать их поддержку. Командлет `Invoke-AzRestMethod` просто расширяет ваш набор инструментов.

## <a name="see-also"></a>См. также

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
