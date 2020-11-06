---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562939"
---
# Get-AzureRmVirtualWan

## КРАТКИй обзор
Возвращает виртуальную глобальную сеть или все виртуальные глобальные ресурсы в группе ресурсов или подписке.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ListBySubscriptionId (по умолчанию)
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListByResourceGroupName
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Возвращает виртуальную глобальную сеть или все виртуальные глобальные ресурсы в группе ресурсов или подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

Эта команда получает виртуальную глобальную сеть с именем myVirtualWAN в группе ресурсов testRG.

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
Название ресурса.

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

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
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVirtualWan

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
