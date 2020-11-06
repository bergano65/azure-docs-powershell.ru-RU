---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561736"
---
# Get-AzureRmLocationBasedServicesAccount

## КРАТКИй обзор
Возвращает учетную запись.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ResourceGroupParameterSet (по умолчанию)
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmLocationBasedServicesAccount** получает учетную запись службы на основе расположения в соответствии с группой ресурсов и именем либо идентификатором ресурса.

Кроме того, он может возвращать список всех учетных записей в ResourceGroup или все учетные записи служб на основе расположения для текущей подписки.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

Возвращает учетную запись с именем Моя учетная запись в группе ресурсов MyResourceGroup, если она существует.

### Пример 2
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

Получает все учетные записи служб на основе расположения в группе ресурсов MyResourceGroup.

### Пример 3
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

Получает все учетные записи служб на основе расположения в текущей подписке.

### Пример 4
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

Получает учетную запись служб на основе расположения, указанную идентификатором ресурса.

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
Имя учетной записи служб на основе местоположения.

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ResourceId (учетная запись) служб на основе местоположения.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount
Этот командлет возвращает объект **PSLocationBasedServicesAccount** .
Вы можете изменить этот объект, а затем применить изменения с помощью **Set-AzureRmLocationBasedServices**.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
