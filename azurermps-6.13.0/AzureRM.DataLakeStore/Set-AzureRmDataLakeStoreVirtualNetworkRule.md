---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563083"
---
# Set-AzureRmDataLakeStoreVirtualNetworkRule

## КРАТКИй обзор
Изменяет указанное правило виртуальной сети в указанном Data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmDataLakeStoreVirtualNetworkRule** изменяет указанное правило виртуальной сети в указанном Data Lake Store.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

Обновление идентификатора подсети правила виртуальной сети "myVNET" в учетной записи "списки рассылки" на "updatedId"

## ПАРАМЕТРЫ

### -Account (учетная запись)
Учетная запись Data Lake Store для обновления правила виртуальной сети

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name (имя)
Имя правила виртуальной сети.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Начало диапазона допустимых IP-адресов для правила виртуальной сети

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
