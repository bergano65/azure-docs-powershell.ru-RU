---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 1a48438d6cec1621361a00cefa2bfead28117b97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960563"
---
# New-AzMlWebService

## SYNOPSIS
Создает веб-службу.

## СИНТАКСИС

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Создает веб-службу машинного обучения Azure в существующей группе ресурсов.
Если в группе ресурсов есть веб-служба с таким же именем, вызов будет обновяться, а существующая веб-служба будет перезаписана.

## ПРИМЕРЫ

### Пример 1. Создание службы на основе определения Json
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Создает веб-службу машинного обучения Azure "mywebservicename" в группе myresourcegroup и регионе "Южный центр США" на основе определения, представленного в файле json, на который имеется ссылка.

### Пример 2. Создание службы из экземпляра объекта
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Вы можете получить экземпляр объекта веб-службы, который нужно настроить перед публикацией в качестве ресурса, с помощью Import-AzMlWebService-управления.

## PARAMETERS

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

### -DefinitionFile
Путь к файлу, содержащего определение формата JSON веб-службы.
Последнюю спецификацию определения веб-службы можно найти в swagger spec в https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning области .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Не спрашивайте подтверждения.

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
Регион веб-службы.
Введите регион центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия".
Вы можете разместить веб-службу в любом регионе, который поддерживает ресурсы такого типа.
Веб-служба не должна быть в том же регионе, что и в подписке Azure, или в том же регионе, что и группа ресурсов.
Группы ресурсов могут содержать веб-службы из разных регионов.
Чтобы определить, в каких регионах поддерживается каждый тип ресурсов, используйте Get-AzResourceProvider с помощью Get-AzResourceProvider параметра ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя веб-службы.
Имя должно быть уникальным в группе ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
Определение для новой веб-службы, содержащее все свойства, которые ее составляют.
Этот параметр является required и представляет экземпляр класса Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.
Последнюю спецификацию определения веб-службы можно найти в swagger spec в https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json области .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов, в которую нужно разместить веб-службу.
Введите регион центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия".
Вы можете разместить веб-службу в любом регионе, который поддерживает ресурсы такого типа.
Веб-служба не должна быть в том же регионе, что и в подписке Azure, или в том же регионе, что и группа ресурсов.
Группы ресурсов могут содержать веб-службы из разных регионов.
Чтобы определить, в каких регионах поддерживается каждый тип ресурсов, используйте Get-AzResourceProvider с помощью Get-AzResourceProvider параметра ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## OUTPUTS

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## ПРИМЕЧАНИЯ
Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## СВЯЗАННЫЕ ССЫЛКИ
