---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423671"
---
# Set-AzResource

## SYNOPSIS
Изменяет ресурс.

## СИНТАКСИС

### ByResourceId (по умолчанию)
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByInputObject
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BySubscriptionLevel
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTenantLevel
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
В этом режиме существующий ресурс Azure изменяется с использованием **cmdlet Set-AzResource.**
Укажите ресурс, который нужно изменить по имени, типу или по коду.

## ПРИМЕРЫ

### Пример 1. Изменение ресурса
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

Первая команда получает ресурс ContosoSite с помощью командлета Get-AzResource, а затем сохраняет его в $Resource переменной.
Вторая команда изменяет свойство $Resource.
Конечная команда обновляет ресурс в $Resource.

### Пример 2. Изменение всех ресурсов в заданной группе ресурсов
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

Первая команда получает ресурсы в группе ресурсов testrg, а затем сохраняет их в переменной $Resource.

Вторая команда итерирует каждый из этих ресурсов в группе ресурсов и добавляет к ним новый тег.

Конечная команда обновляет каждый из этих ресурсов.

## PARAMETERS

### -ApiVersion
Определяет версию API поставщика ресурсов.
Если не указать версию, этот cmdlet использует последнюю доступную версию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Запуск cmdlet в фоновом режиме

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
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionResourceName
Указывает имя ресурса расширения.
Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных "Имя сервера".

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionResourceType
Тип ресурса для ресурса расширения.
Например, если ресурсом расширения является база данных, укажите следующее: `Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Запуск команды без запроса подтверждения.

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

### -InputObject
Объектное представление ресурса, который нужно обновить.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kind
Определяет тип ресурса.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Указывает фильтр стилей Open Data Protocol (OData).
Этот cmdlet добавит это значение к запросу в дополнение к любым другим фильтрам.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan
Определяет свойства плана ресурсов (в качестве hash table) для ресурса.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.

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

### -Properties
Определяет свойства ресурса.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, для которой этот cmdlet изменяет ресурс.

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Указывает полностью определенный ИД ресурса, включая подписку, как по следующему примеру: `/subscriptions/` ИД подписки.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Указывает имя ресурса.
Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Тип ресурса.
Например, для базы данных тип ресурса: `Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Указывает объект SKU ресурса в качестве hash table.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Пары значений ключа в виде hash table. Например: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantLevel
Указывает на то, что этот cmdlet работает на уровне клиента.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePatchSemantics
Указывает на то, что для обновления объекта с помощью этого cmdlet используется HTTP-ИСПРАВЛЕНИЕ, а не HTTP PUT.

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

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource

### System.String

### System.Management.Automation.PSObject

### System.Collections.Hashtable

## OUTPUTS

### System.Management.Automation.PSObject

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzResource](./Get-AzResource.md)

[Move-AzResource](./Move-AzResource.md)

[New-AzResource](./New-AzResource.md)

[Remove-AzResource](./Remove-AzResource.md)
