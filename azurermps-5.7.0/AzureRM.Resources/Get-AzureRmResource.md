---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563327"
---
# Get-AzureRmResource

## КРАТКИй обзор
Возвращает ресурсы.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### GetAllResources (по умолчанию)
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceId
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByTenantLevel
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecifiedScopeAtTenantLevel
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByNameAndGroup
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceNameAndType
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByNameGroupAndType
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetResourceCollection
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmResource** получает ресурсы Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех ресурсов определенного типа
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

Эта команда возвращает ресурс типа Microsoft. Web/Sites в разделе ResourceGroup11.

### Пример 2: получение ресурса по имени
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

Эта команда получает ресурс с именем ContosoWebsite в разделе ResourceGroup11.

### Пример 3: отображение всех состояний учетных записей хранения в группе ресурсов
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## ПАРАМЕТРЫ

### -ApiVersion
```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandProperties
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionResourceName
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionResourceType
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IsCollection
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере: 

`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`

Этот командлет получает ресурс с таким ИДЕНТИФИКАТОРом.

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantLevel
Указывает на то, что этот командлет работает на уровне клиента.

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### System. Management. Automation. PSObject

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Find-AzureRmResource](./Find-AzureRmResource.md)

[Move-AzureRmResource](./Move-AzureRmResource.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Set-AzureRmResource](./Set-AzureRmResource.md)


