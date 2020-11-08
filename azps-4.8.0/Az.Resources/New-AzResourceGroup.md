---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077652"
---
# New-AzResourceGroup

## КРАТКИй обзор
Создание группы ресурсов Azure.

## Максимальное

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzResourceGroup** создает группу ресурсов Azure.
Вы можете создать группу ресурсов, используя только имя и расположение, а затем с помощью командлета New-AzResource создать ресурсы, которые нужно добавить в группу ресурсов.
Чтобы добавить развертывание в существующую группу ресурсов, используйте командлет New-AzResourceGroupDeployment. Чтобы добавить ресурс в существующую группу ресурсов, используйте командлет **New-AzResource** . Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт. Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание пустой группы ресурсов
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Эта команда создает группу ресурсов, в которой нет ресурсов. Вы можете использовать командлеты **New-AzResource** или **New-AzResourceGroupDeployment** для добавления ресурсов и развертываний в эту группу ресурсов.

### Пример 2: создание пустой группы ресурсов с помощью позиционных параметров
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Эта команда создает группу ресурсов, в которой нет ресурсов.

### Пример 3: создание группы ресурсов с помощью тегов
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Эта команда создает пустую группу ресурсов. Эта команда аналогична команде в примере 1, за исключением того, что она назначает теги для группы ресурсов. Первый тег, именуемый Empty, можно использовать для идентификации групп ресурсов, не имеющих ресурсов. Второй тег называется "Отдел" и имеет значение "маркетинг". Вы можете использовать тег, например этот, для классификации групп ресурсов для администрирования и бюджетирования.

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию API, поддерживаемую поставщиком ресурсов.
Вы можете выбрать версию, отличную от версии по умолчанию.

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
Принудительное выполнение команды без запроса подтверждения пользователя.

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
Указывает расположение группы ресурсов. Укажите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии. Группу ресурсов можно поместить в любое место. Группа ресурсов может не находиться в той же папке, в которой находится подписка на Azure, или в том же местоположении, что и его ресурсы.
Чтобы определить, в каком месте поддерживается каждый тип ресурсов, используйте командлет Get-AzResourceProvider с параметром *ProviderNamespace* .

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

### -Name (имя)
Указывает имя группы ресурсов. Имя ресурса должно быть уникальным в рамках подписки. Если группа ресурсов с таким именем уже существует, она запрашивает подтверждение перед тем, как заменить существующую группу ресурсов.

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
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

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

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"} чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.
Определив теги для ресурсов и групп, вы можете использовать параметр *Tag* Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени тега или по имени и значению. Теги можно использовать для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.
Чтобы получить предопределенные теги, используйте командлет Get-AzTag.

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Collections. Hashtable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroup

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
