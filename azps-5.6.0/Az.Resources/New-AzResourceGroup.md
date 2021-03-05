---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008611"
---
# New-AzResourceGroup

## SYNOPSIS
Создает группу ресурсов Azure.

## СИНТАКСИС

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для **этого создается** группа ресурсов Azure.
Вы можете создать группу ресурсов, используя только имя и расположение, а затем использовать New-AzResource для создания ресурсов для добавления в группу ресурсов.
Чтобы добавить развертывание в существующую группу ресурсов, воспользуйтесь New-AzResourceGroupDeployment управления. Чтобы добавить ресурс в существующую группу ресурсов, воспользуйтесь **cmdlet New-AzResource.** Ресурс Azure — это объект Azure, управляемый пользователем, например сервер базы данных, база данных или веб-сайт. Группа ресурсов Azure — это набор ресурсов Azure, развертываемых в качестве единицы.

## ПРИМЕРЫ

### Пример 1. Создание пустой группы ресурсов
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Эта команда создает группу ресурсов без ресурсов. Для добавления ресурсов и развертывания в эту группу ресурсов можно использовать **new-AzResource** или **New-AzResourceGroupDeployment.**

### Пример 2. Создание пустой группы ресурсов с использованием позиционной параметров
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Эта команда создает группу ресурсов без ресурсов.

### Пример 3. Создание группы ресурсов с тегами
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Эта команда создает пустую группу ресурсов. Эта команда та же, что и в примере 1, за исключением того, что она назначает теги группе ресурсов. Первый тег с именем "Пусто" можно использовать для определения групп ресурсов, не имеющих ресурсов. Второй тег называется "Отдел" и имеет значение "Маркетинг". С помощью такого тега можно классифицировать группы ресурсов для администрирования или бюджетизации.

## PARAMETERS

### -ApiVersion
Указывает версию API, которая поддерживается поставщиком ресурсов.
Можно указать другую версию, чем версия по умолчанию.

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

### -Location
Определяет расположение группы ресурсов. Укажите расположение центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия". Группу ресурсов можно разместить в любом месте. Группа ресурсов не должна быть расположена в том же расположении, что и ее подписка На Azure.
Чтобы определить, какое расположение поддерживает каждый тип ресурсов, используйте Get-AzResourceProvider с параметром *ProviderNamespace.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Имя группы ресурсов. Имя ресурса должно быть уникальным в подписке. Если группа ресурсов с таким именем уже существует, перед заменой существующей группы ресурсов будет предложено подтвердить ее.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
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

### -Tag
Пары "ключевое значение" в виде hash table. Например: @{key0="value0";key1=$null;key2="value2"} Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.
После назначения тегов ресурсам и группам можно  использовать параметр "Тег" в Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению. С помощью тегов можно классифицировать ресурсы,например по отделам или затратам, а также для отслеживания заметок и примечаний к ресурсам.
Чтобы получить предопределные теги, воспользуйтесь Get-AzTag командлетом.

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

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
