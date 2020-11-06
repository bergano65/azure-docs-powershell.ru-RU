---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566140"
---
# Find-AzureRmResource

## КРАТКИй обзор
Осуществляет поиск ресурсов на основе указанных параметров.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### GetBySpecifiedScope (по умолчанию)
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetBySpecifiedScopeAtTenantLevel
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### GetByMultiSubscriptionQuery
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetByTagObject
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### GetByTagNameValue
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Find-AzureRmResource** выполняет поиск ресурсов на основе указанных параметров.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Поиск ресурсов по типам и именам групп ресурсов
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

Эта команда ищет ресурсы типа Microsoft. Web/Sites в группах ресурсов, имена которых соответствуют строковому элементу ResourceGroup.

### Пример 2: Поиск ресурсов по типу и названию ресурса
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

Эта команда осуществляет поиск ресурсов типа Microsoft. Web/Sites с именем ресурса, совпадающим с тестовым строкой.

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию используемого API поставщика ресурсов.
Если вы не укажете версию, этот командлет использует последнюю доступную версию.

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
Указывает на то, что этот командлет расширяет свойства ресурса.

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

### -ExtensionResourceType
Указывает тип ресурсов расширения для ресурсов, которые выполняет этот командлет.
Например:

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
Задает фильтр стиля Open Data Protocol (OData).
Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.

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
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

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

### -ResourceGroupNameContains
Указывает частичное имя группы ресурсов.
Этот командлет соответствует группам ресурсов, для которых это значение является подстрокой.
Командлет выполнит поиск ресурсов в этих группах ресурсов.

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupNameEquals
Имя группы ресурсов для полного соответствия.

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceNameContains
Указывает частичное имя ресурса.
Командлет ищет ресурсы, содержащие это значение, в виде подстроки.

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceNameEquals
Имя ресурса для полного соответствия. Например, если имя ресурса — testResource, вы можете указать testResource.

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Указывает тип ресурса.
Например, для базы данных тип ресурса выглядит следующим образом:

`Microsoft.Sql/Servers/Databases`

Этот командлет осуществляет поиск ресурсов указанного типа.

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Фильтр тегов для запроса OData. Ожидаемый формат: @ {tagName = $null} или @ {tagName = ' tagValue '}.

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TagName
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantLevel
Указывает на то, что этот командлет работает на уровне клиента.

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Указывает количество извлекаемых ресурсов.

```yaml
Type: Int32
Parameter Sets: (All)
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

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Move-AzureRmResource](./Move-AzureRmResource.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Set-AzureRmResource](./Set-AzureRmResource.md)
