---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 2ae475d28584a90a0255a27d79cdbddbbccdcdd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563599"
---
# Remove-AzureRmDataLakeAnalyticsFirewallRule

## КРАТКИй обзор
Удаляет правило брандмауэра из учетной записи Data Lake Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmDataLakeAnalyticsFirewallRule** удаляет правило брандмауэра из учетной записи Azure Data Lake Analytics.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление правила брандмауэра
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

Эта команда удаляет правило брандмауэра с именем "Мое правило брандмауэра" из учетной записи "ContosoAdlAcct"

## ПАРАМЕТРЫ

### -Account (учетная запись)
Учетная запись Data Lake Analytics, из которой нужно удалить правило межсетевого экрана

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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
Имя правила брандмауэра.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которой требуется получить учетную запись.

```yaml
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
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
System. Management. Automation. SwitchParameter

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

