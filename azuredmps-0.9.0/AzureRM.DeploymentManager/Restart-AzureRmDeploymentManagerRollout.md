---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556084"
---
# Restart-AzureRmDeploymentManagerRollout

## КРАТКИй обзор
Перезапустите развертывание с ошибкой.

## Максимальное

### Интерактивный (по умолчанию)
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **restarting-AzureRmDeploymentManagerRollout** перезапускает сбой и возвращает объект, который представляет собой все подробные сведения о ходе выпуска.
Укажите имя и имя группы ресурсов. Кроме того, можно предоставить объект выпуска или ИД ресурса.
Необязательный параметр SkipSucceeded позволяет пропустить все этапы, успешно описанные в предыдущем запуске выпуска.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

Эта команда перезапускает выгрузку с именем ContosoRollout в ContosoResourceGroup. Флаг SkipSucceeded указывает на то, что все шаги, которые уже выполнялись успешно, должны быть пропущены, а выпуск должен продолжить выполнение с того места, на котором он завершился последним сбоем.

### Пример 2: перезапуск выпуска с помощью идентификатора ресурса
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Эта команда перезапускает выгрузку с именем ContosoRollout в ContosoResourceGroup.

### Пример 3. Перезапустите развертывание с помощью объекта выпуска.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Эта команда перезапускает выгрузку, имя и значение ResourceGroup которой совпадают со свойствами Name и ResourceGroupName в $rolloutObject соответственно.

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
Имя выпуска.

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

### -Выпуск
Ресурс, который нужно удалить.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SkipSucceeded
Пропустите шаги, которые были выполнены в предыдущем запуске выпуска.

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

### Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmDeploymentManagerRollout](./Get-AzureRmDeploymentManagerRollout.md)

[Остановить-AzureRmDeploymentManagerRollout](./Stop-AzureRmDeploymentManagerRollout.md)

[Remove-AzureRmDeploymentManagerRollout](./Remove-AzureRmDeploymentManagerRollout.md)