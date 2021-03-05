---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971608"
---
# Remove-AzSynapseSqlPoolRestorePoint

## SYNOPSIS
Удаляет синапсексическую аналитику SQL точки восстановления пула.

## СИНТАКСИС

### DeleteByNameParameterSet (по умолчанию)
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteByParentObjectParameterSet
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeleteByInputObjectParameterSet
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteByResourceIdParameterSet
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его** SQL точки восстановления пула навсегда удаляется SQL Azure Synapse Analytics.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

Эта команда удаляет точки восстановления пула SQL Azure Synapse Analytics.

### Пример 2
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL через канал.

### Пример 3
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL через канал.

### Пример 4
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

Эта команда удаляет точки SQL Azure Synapse Analytics с указанным ИД ресурса.

## PARAMETERS

### -AsJob
Запуск cmdlet в фоновом режиме

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -InputObject
SQL создания точки восстановления пула входной объект времени создания, как правило, передается по конвейеру.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя SQL Synapse.

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Этот cmdlet не возвращает объект по умолчанию. Если этот переключатель задан, возвращается истина, если он успешен.

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

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса в SQL Synapse.

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RestorePointCreationDate
Имя синтаксиса SQL даты создания точки восстановления.

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlPoolObject
Входной объект SQL Pool обычно передается по конвейеру.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Имя рабочей области Synapse.

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool

### Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint

### System.String

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
