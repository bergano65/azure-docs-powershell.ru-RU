---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566186"
---
# Get-AzureRmDataMigrationService

## КРАТКИй обзор
Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ResourceGroupSet (по умолчанию)
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### ResourceIdParameterSet
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### ServiceNameGroupSet
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## NОПИСАНИЕ
Командлет Get-AzureRmDataMigrationService извлекает свойства, связанные с экземпляром службы миграции баз данных Azure, на основе имени службы и имени группы ресурсов Azure в качестве входных параметров. 

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

В приведенном выше примере извлекаются свойства экземпляра службы миграции баз данных Azure с именем testService. 

### Пример 2
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

В приведенном выше примере выполняется получение служб миграции баз данных Azure в группе ресурсов с именем testResourceGroup. 

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя службы миграции данных.

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса DataMigrationService.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

### System. String


## НАПРЯЖЕНИЕ

### System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. Migration, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]]


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ





