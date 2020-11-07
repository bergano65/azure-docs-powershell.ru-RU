---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734457"
---
# New-AzureRmDataMigrationService

## КРАТКИй обзор
Создание нового экземпляра службы миграции баз данных Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## NОПИСАНИЕ
Командлет New-AzureRmDataMigrationService создает новый экземпляр службы миграции баз данных Azure. Этот командлет принимает имя существующей группы ресурсов Azure, уникальное имя для нового экземпляра службы миграции баз данных Azure, область, в которой выполняется подготовка экземпляра, имя SKU рабочего процесса DMS и имя виртуальной подсети Azure, в которой будет находиться служба. Для имени подписки нет параметра, так как ожидается, что пользователь должен указать подписку по умолчанию для сеанса входа Azure или выполнить Get-AzureRmSubscription-SubscriptionName "MySubscription" | Select-AzureRmSubscription, чтобы выбрать другую подписку.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

В приведенном выше примере показано, как создать новый экземпляр службы миграции баз данных Azure с именем TestService в центральном регионе США.


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

### -Location
Расположение создаваемого экземпляра службы миграции баз данных Azure, которое соответствует региону Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Имя экземпляра службы миграции баз данных Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
SKU для экземпляра службы миграции баз данных Azure. В настоящее время доступны значения Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualSubnetId
Имя подсети в указанной виртуальной сети, используемой для экземпляра службы миграции баз данных Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

