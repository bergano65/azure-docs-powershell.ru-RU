---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8068a560954d94a134205d5e67eab19e641bed74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566517"
---
# Get-AzureRmDataFactoryV2LinkedService

## КРАТКИй обзор
Получение сведений о связанных службах в фабрике данных.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByFactoryName (по умолчанию)
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmDataFactoryV2LinkedService получает сведения о связанных службах в фабрике данных Azure.
Если указать имя связанной службы, этот командлет получает сведения о связанной службе.
Если имя не задано, этот командлет получает сведения обо всех связанных службах в фабрике данных.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех связанных службах
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

Эта команда получает сведения обо всех связанных службах в фабрике данных с именем WikiADF, а затем передает связанные службы командлету Format-List с помощью оператора конвейера.
Этот командлет Windows PowerShell форматирует результаты.
Чтобы получить дополнительные сведения, введите Get-Help Format-List.
Вы можете использовать один из указанных ниже способов.

### Пример 2: получение сведений о конкретной связанной службе
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

Эта команда получает сведения о связанной службе с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.

### Пример 3: получение сведений о конкретной связанной службе путем указания параметра "фактическое значение"
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Первая команда использует командлет Get-AzureRmDataFactoryV2 для получения фабрики данных с именем ContosoFactory, а затем сохраняет ее в переменной $DataFactory.
Вторая команда получает сведения о связанной службе для фабрики данных, хранящейся в $DataFactory, а затем передает эти данные командлету Format-Table с помощью оператора конвейера.
Командлет Format-Table форматирует выходные данные в виде набора данных с указанными свойствами в качестве столбцов набора данных.

## ПАРАМЕТРЫ

### — Фактическое.
Указывает объект PSDataFactory.
Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Указывает имя фабрики данных.
Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя связанной службы, сведения о которой требуется получить.

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет получает связанные службы, которые относятся к группе, которую указывает этот параметр.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса Azure.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Параметры: фактическое (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRmDataFactoryV2LinkedService]()

[Remove-AzureRmDataFactoryV2LinkedService]()
