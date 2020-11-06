---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: fabe9019ff1a793bf5c7b5b0608f63ea4d9881f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561539"
---
# New-AzureRmResourceGroup

## КРАТКИй обзор
Создание группы ресурсов Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmResourceGroup** создает группу ресурсов Azure.

Вы можете создать группу ресурсов, используя только имя и расположение, а затем с помощью командлета New-AzureRmResource создать ресурсы, которые нужно добавить в группу ресурсов.

Чтобы добавить развертывание в существующую группу ресурсов, используйте командлет New-AzureRmResourceGroupDeployment. Чтобы добавить ресурс в существующую группу ресурсов, используйте командлет **New-AzureRmResource** . Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт. Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание пустой группы ресурсов
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

Эта команда создает группу ресурсов, в которой нет ресурсов. Вы можете использовать командлеты **New-AzureRmResource** или **New-AzureRmResourceGroupDeployment** для добавления ресурсов и развертываний в эту группу ресурсов.

### Пример 2: создание пустой группы ресурсов с помощью позиционных параметров
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

Эта команда создает группу ресурсов, в которой нет ресурсов.

### Пример 3: создание группы ресурсов с помощью тегов
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Эта команда создает пустую группу ресурсов. Эта команда аналогична команде в примере 1, за исключением того, что она назначает теги для группы ресурсов. Первый тег, именуемый Empty, можно использовать для идентификации групп ресурсов, не имеющих ресурсов. Второй тег называется "Отдел" и имеет значение "маркетинг". Вы можете использовать тег, например этот, для классификации групп ресурсов для администрирования и бюджетирования.

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию API, поддерживаемую поставщиком ресурсов.
Вы можете выбрать версию, отличную от версии по умолчанию.

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

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

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

### -Location
Указывает расположение группы ресурсов. Укажите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии. Группу ресурсов можно поместить в любое место. Группа ресурсов может не находиться в той же папке, в которой находится подписка на Azure, или в том же местоположении, что и его ресурсы.

Чтобы определить, в каком месте поддерживается каждый тип ресурсов, используйте командлет Get-AzureRmResourceProvider с параметром *ProviderNamespace* .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя группы ресурсов. Имя ресурса должно быть уникальным в рамках подписки. Если группа ресурсов с таким именем уже существует, она запрашивает подтверждение перед тем, как заменить существующую группу ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.

Определив теги для ресурсов и групп, вы можете использовать параметр *Tag* Get-AzureRmResource и Get-AzureRmResourceGroup для поиска ресурсов и групп по имени тега или по имени и значению. Теги можно использовать для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.

Чтобы получить предопределенные теги, используйте командлет Get-AzureRMTag.

```yaml
Type: Hashtable
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)
