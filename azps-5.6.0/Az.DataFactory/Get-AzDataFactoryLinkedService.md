---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975416"
---
# Get-AzDataFactoryLinkedService

## SYNOPSIS
Получает сведения о связанных службах в фабрике данных Azure.

## СИНТАКСИС

### ByFactoryName (По умолчанию)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для получения сведений о связанных службах в фабрике данных Azure можно получить сведения о **cmdlet Get-AzDataFactoryLinkedService.**
Если указать имя связанной службы, этот cmdlet получит сведения о связанной службе.
Если имя не указано, этот cmdlet получает сведения обо всех связанных службах в фабрике данных.

## ПРИМЕРЫ

### Пример 1. Сведения обо всех связанных службах
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Эта команда получает сведения обо всех связанных службах в фабрике данных Под названием WikiADF, а затем передает связанные службы в командлет Format-List с помощью оператора конвейера.
Этот cmdlet formats the results (Форматирование результатов).
Для получения дополнительных сведений введите `Get-Help Format-List` .

### Пример 2. Просмотр сведений о конкретной связанной службе
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Эта команда получает сведения о связанной службе HDILinkedService в фабрике данных с именем WikiADF.

### Пример 3. Получите сведения об определенной связанной службе, указав параметр DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Первая команда использует Get-AzDataFactory для получения фабрики данных ContosoFactory, а затем сохраняет ее в переменной $DataFactory.
Вторая команда получает сведения о связанной службе для фабрики данных, храняной в $DataFactory, а затем передает ее командлету Format-Table с помощью оператора конвейера.
**Format-Table** форматирование вывода в виде наборов данных с указанными свойствами в качестве столбцов для наборов данных.

## PARAMETERS

### -DataFactory
Указывает объект **PSDataFactory.**
Этот cmdlet получает связанные службы, которые относятся к фабрике данных, указанной этим параметром.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Название фабрики данных.
Этот cmdlet получает связанные службы, которые относятся к фабрике данных, указанной этим параметром.

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

### -Name
Указывает имя связанной службы, сведения о которой нужно получить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов Azure.
Этот cmdlet получает связанные службы, которые относятся к группе, указанной этим параметром.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


