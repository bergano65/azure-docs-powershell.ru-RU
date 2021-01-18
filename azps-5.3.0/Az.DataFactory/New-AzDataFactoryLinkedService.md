---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518961"
---
# New-AzDataFactoryLinkedService

## SYNOPSIS
Связывает хранилище данных или облачную службу с фабрикой данных Azure.

## СИНТАКСИС

### ByFactoryName (По умолчанию)
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet New-AzDataFactoryLinkedService** связывает хранилище данных или облачную службу с фабрикой данных Azure.
Если указать имя связанной службы, которая уже существует, этот cmdlet запросит подтверждение перед заменой связанной службы.
Если указать параметр *Force,* то вместо существующей связанной службы не будет подтверждения.
Выполните эти действия в следующем порядке: 
- Создание фабрики данных. 
- Создание связанных служб. 
- Создание наборов данных. 
- Создание конвейера.

## ПРИМЕРЫ

### Пример 1. Создание связанной службы
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.
Эта связанная служба связывает указанное в файле хранилище BLOB-приложений Azure с фабрикой данных с именем WikiADF.
Команда передает результат командлету Format-List с помощью оператора конвейера.
Это Windows PowerShell форматирование результатов.
Для получения дополнительных сведений введите `Get-Help Format-List` .

## PARAMETERS

### -DataFactory
Указывает объект **PSDataFactory.**
Этот cmdlet создает связанную службу для фабрики данных, указанной этим параметром.

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
Этот cmdlet создает связанную службу для фабрики данных, указанной этим параметром.

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

### -File
Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание связанной службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Указывает на то, что этот cmdlet заменяет существующую связанную службу без запроса подтверждения.

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

### -Name
Указывает имя связанной службы, которая будет создаваться.

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
Указывает имя группы ресурсов Azure.
Этот cmdlet создает связанную службу для группы, указанной этим параметром.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzDataFactoryLinkedService](./Get-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


