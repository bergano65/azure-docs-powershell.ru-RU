---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012595"
---
# Get-AzConfluentOrganization

## SYNOPSIS
Получите свойства определенного ресурса организации.

## СИНТАКСИС

### Список (по умолчанию)
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### List1
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
Получите свойства определенного ресурса организации.

## ПРИМЕРЫ

### Пример 1. Список всех организаций с слиянием в рамках подписки
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

Эта команда содержит список всех организаций, которые имеют подписку.

### Пример 2. Список всех организаций, объединенных в группу ресурсов
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

Эта команда содержит список всех организаций, объединенных в группу ресурсов.

### Пример 3. Организация с слиянием по имени
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

Эта команда получает организацию по имени.

### Пример 4. Организация с каналом слияния
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

Эта команда получает организацию в канале слияния.

## PARAMETERS

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

### -InputObject
Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Название ресурса организации

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД подписки Microsoft Azure

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IConfluentIdentity> : Параметр identity
  - `[Id <String>]`: путь удостоверения ресурса
  - `[OrganizationName <String>]`: название ресурса организации
  - `[ResourceGroupName <String>]`: имя группы ресурсов
  - `[SubscriptionId <String>]`: ИД подписки Microsoft Azure

## СВЯЗАННЫЕ ССЫЛКИ

