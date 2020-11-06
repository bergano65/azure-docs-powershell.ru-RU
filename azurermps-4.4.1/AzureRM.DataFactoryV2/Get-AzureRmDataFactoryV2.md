---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566270"
---
# Get-AzureRmDataFactoryV2

## КРАТКИй обзор
Получает сведения о фабрике данных.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmDataFactoryV2 получает сведения о фабриках данных в группе ресурсов Azure.
Если вы задаете имя фабрики данных, этот командлет получает сведения о фабрике данных.
Если имя не задано, этот командлет получает сведения обо всех фабриках данных в группе ресурсов Azure.


## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех фабрик данных
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

Отображает сведения обо всех фабриках данных в подписке Azure.

### Пример 2: получение определенной фабрики данных
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов с именем ADF и сохраняет ее в переменной $DataFactory.
Укажите параметр фактического значения в последующих командлетах для использования фабрики данных, хранящейся в $DataFactory.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя фабрики данных, сведения о которой требуется получить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет получает сведения о фабриках данных, относящихся к группе. Этот параметр указывает.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

### System. String


## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory


## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
[Set-AzureRmDataFactoryV2]()

[Remove-AzureRmDataFactoryV2]()

