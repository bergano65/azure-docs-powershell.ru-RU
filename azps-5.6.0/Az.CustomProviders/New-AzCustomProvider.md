---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: a3180cd693ae4c234656ba5d0812900ce8c308b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998133"
---
# New-AzCustomProvider

## SYNOPSIS
Создание или обновление пользовательского поставщика ресурсов.

## СИНТАКСИС

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Создание или обновление пользовательского поставщика ресурсов.

## ПРИМЕРЫ

### Пример 1. Создание пользовательского поставщика
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Создание пользовательского поставщика ресурсов

### Пример 2. Создание пользовательского поставщика с связи
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Создайте пользовательского поставщика с маршрутом для его объединений.

## PARAMETERS

### -Action
Список действий, которые реализует настраиваемый поставщик ресурсов.
Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств ACTION и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Запуск команды в качестве задания

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Расположение ресурса

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя поставщика ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Запуск команды асинхронно

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Список типов ресурсов, которые реализует настраиваемый поставщик ресурсов.
Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств RESOURCETYPE и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД подписки Azure.
Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Теги ресурсов

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Проверка
Список проверки, которые нужно выполнить по запросам поставщика ресурсов.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств проверки и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


ACTION <ICustomRpActionRouteDefinition[]>: список действий, которые реализует поставщик ресурсов.
  - `Endpoint <String>`: URI конечной точки определения маршрутов, к который настраиваемый поставщик ресурсов будет запрашивать у поставщика прокси-серверов. Это может быть в виде плоского URI (например, ' ') или может указывать маршрут по маршруту https://testendpoint/ (например, ' https://testendpoint/{requestPath} ').
  - `Name <String>`: имя определения маршрута. Оно становится именем расширения ARM (например, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ActionRouting?>]`. Типы маршрутов, поддерживаемые для запросов на действие.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: список типов ресурсов, которые реализует настраиваемый поставщик ресурсов.
  - `Endpoint <String>`: URI конечной точки определения маршрутов, к который настраиваемый поставщик ресурсов будет запрашивать у поставщика прокси-серверов. Это может быть в виде плоского URI (например, ' ') или может указывать маршрут по маршруту https://testendpoint/ (например, ' https://testendpoint/{requestPath} ').
  - `Name <String>`: имя определения маршрута. Оно становится именем расширения ARM (например, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ResourceTypeRouting?>]`. Типы маршрутов, поддерживаемые для запросов ресурсов.

VALIDATION <ICustomRpValidations[]>: список проверки для запуска по запросам поставщика ресурсов.
  - `Specification <String>`: ссылка на спецификацию проверки. Спецификацию необходимо разо всех raw.githubusercontent.com.
  - `[ValidationType <ValidationType?>]`. Тип проверки, которая будет запускаться для запроса на соответствие.

## СВЯЗАННЫЕ ССЫЛКИ

