---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: d31af9321a474c1261b2ed75138696d9f1a45461
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562023"
---
# Set-AzureRmSqlDatabaseRecommendedActionState

## КРАТКИй обзор
Обновляет состояние рекомендуемого действия для базы данных SQL Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmSqlDatabaseRecommendedActionState** обновляет состояние рекомендуемого действия базы данных Azure SQL.
Это позволяет применять рекомендованное действие, возвращая или удаляя его в зависимости от нового состояния.

## ИЛЛЮСТРИРУЮТ

### Пример 1: применение рекомендуемого состояния действия к ожиданию
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

Эта команда обновляет состояние рекомендуемого действия с именем IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893, которое принадлежит базе данных с именем WIRunner, в ожидание.

## ПАРАМЕТРЫ

### -AdvisorName
Указывает имя помощника, которому принадлежит рекомендуемое действие.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Указывает имя базы данных, для которой этот командлет задает рекомендуемое состояние действия.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecommendedActionName
Указывает имя рекомендуемого действия, для которого обновляется состояние.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов для сервера, который содержит эту базу данных.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера базы данных.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Указывает новое значение, на которое этот командлет обновляет рекомендуемое состояние действия.

Для этого параметра допустимы следующие значения:

- Службы
- Типа
- PendingRevert
- RevertCancelled
- Учитываться
- Разрешившего

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база_данных, MSSQL, Advisor, recommendedaction

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlServerAdvisor](./Get-AzureRmSqlServerAdvisor.md)

[Get-AzureRmSqlElasticPoolAdvisor](./Get-AzureRmSqlElasticPoolAdvisor.md)

[Get-AzureRmSqlServerRecommendedAction](./Get-AzureRmSqlServerRecommendedAction.md)

[Get-AzureRmSqlElasticPoolRecommendedAction](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[Set-AzureRmSqlElasticPoolRecommendedActionState](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Set-AzureRmSqlElasticPoolRecommendedActionState](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[Set-AzureRmSqlServerRecommendedActionState](./Set-AzureRmSqlServerRecommendedActionState.md)

[Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Set-AzureRmSqlServerAdvisorAutoExecuteStatus](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)
