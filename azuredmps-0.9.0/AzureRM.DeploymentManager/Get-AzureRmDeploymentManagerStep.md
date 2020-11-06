---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555415"
---
# Get-AzureRmDeploymentManagerStep

## КРАТКИй обзор
Получает шаг развертывания.

## Максимальное

### Интерактивный (по умолчанию)
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmDeploymentManagerStep** получает шаг и возвращает объект, который представляет этот шаг.
Укажите шаг, указав имя и имя группы ресурсов. Кроме того, вы можете предоставить объект Step или ResourceId.

Вы можете локально изменить этот объект, а затем применить изменения к источнику артефакта с помощью командлета Set-AzureRmDeploymentManagerStep.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение шага
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.

### Пример 2: получение шага с помощью идентификатора ресурса
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.

### Пример 3: получение шага с помощью объекта, возвращаемого New-AzureRmDeploymentManagerStep
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 Эта команда получает шаг, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $stepObject соответственно.


## ПАРАМЕТРЫ

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
Имя шага.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Шаг
Объект шага "ресурс".

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.
Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
