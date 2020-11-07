---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 325888f510f967f93aca5b3ef50294dd83971213
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720437"
---
# New-AzMlWebService

## КРАТКИй обзор
Создание новой веб-службы.

## Максимальное

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

## NОПИСАНИЕ
Создание веб-службы машинного обучения Azure в существующей группе ресурсов.
Если в группе ресурсов есть веб-служба с таким же именем, вызов выполняет операцию обновления, и существующая веб-служба перезаписывается.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание новой службы из определения на основе JSON-файла
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Создание новой веб-службы машинного обучения Azure с именем "mywebservicename" в группе "myresourcegroup" и в Южной Центральной области США в соответствии с определением, представленным в JSON-файле, на который указывает ссылка.

### Пример 2: создание новой службы из экземпляра объекта
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Вы можете получить экземпляр объекта веб-службы для настройки перед публикацией как ресурс с помощью командлета Import-AzMlWebService.

## ПАРАМЕТРЫ

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
Задает путь к файлу, содержащему определение формата JSON для веб-службы.
Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

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
Не запрашивать подтверждение.

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
Область веб-службы.
Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".
Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.
Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.
Группы ресурсов могут содержать веб-службы из разных регионов.
Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzResourceProvider с командлетом параметра ProviderNamespace.

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

### -Name (имя)
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
Определение новой веб-службы, содержащее все свойства, составляющие службу.
Этот параметр является обязательным и представляет экземпляр класса Microsoft. Azure. Management. MachineLearning. WebService. WebService.
Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

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
Группа ресурсов, в которую нужно поместить веб-службу.
Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".
Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.
Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.
Группы ресурсов могут содержать веб-службы из разных регионов.
Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzResourceProvider с командлетом параметра ProviderNamespace.

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Management. MachineLearning. WebService. Models.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. MachineLearning. WebService. Models.

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
