---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073883"
---
# Sync-AzAnalysisServicesInstance

## КРАТКИй обзор

Синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzAnalysisServicesAccount

## Максимальное

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ

Командлет Sync-AzAnalysisServicesInstance синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в Add-AzAnalysisServicesAccount команде.

## ИЛЛЮСТРИРУЮТ

### Пример 1

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Эта команда синхронизирует базу данных с именем SalesOrders на сервере с именем Contoso в среде westus.asazure.windows.net, в которой пользователь вошел в эту среду с помощью Add-AzAnalysisServicesAccount команды.

## ПАРАМЕТРЫ

### -База данных

Идентификация базы данных, которую нужно синхронизировать

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Instance

Имя экземпляра сервера служб Analysis Services, который нужно перезапустить

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Если указать это, будет возвращено значение истина, если команда была выполнена успешно.

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. AnalysisServices. в плане. Models. ScaleOutServerDatabaseSyncDetails

## Пуск

Alias (псевдоним): Sync-AzAsInstance

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
