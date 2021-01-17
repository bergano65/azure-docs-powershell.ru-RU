---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391975"
---
# Get-AzKustoClusterFollowerDatabase

## SYNOPSIS
Возвращает список баз данных, которые принадлежат этому кластеру и за которыми следует другой кластер.

## СИНТАКСИС

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Возвращает список баз данных, которые принадлежат этому кластеру и за которыми следует другой кластер.

## ПРИМЕРЫ

### Пример 1. Список всех баз данных, на которые вы на которые следуете
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

Указанная выше команда содержит список всех баз данных, которые принадлежат этому кластеру. За ними следует другой кластер.

## PARAMETERS

### -ClusterName
Название кластера "Кусто".

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, содержащей кластер Кусто.

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

### -SubscriptionId
Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.
Он является частью URI каждого звонка службы.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition

## ПРИМЕЧАНИЯ

ALIASES

## СВЯЗАННЫЕ ССЫЛКИ

