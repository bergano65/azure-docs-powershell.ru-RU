---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560399"
---
# Export-AzureAnalysisServicesInstance

## КРАТКИй обзор
Экспортирует журнал из экземпляра сервера служб Analysis Services в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## NОПИСАНИЕ
Командлет Export-AzureAnalysisServicesInstance экспортирует журнал из экземпляра сервера служб аналитики Azure в файл.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

Эта команда будет экспортировать журнал с сервера "TestServer" в среде, указанной в команде Add-AzureAnalysisServicesAccount, и сохранить ее в файле, указанном в элементе OutputPath "C:\path\to\log\testserver.log"

## ПАРАМЕТРЫ

### -Instance
Имя экземпляра сервера служб Analysis Services

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
Выходной путь к файлу для экспорта журнала

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Перезаписать файл, если он существует без запроса

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск
Alias (псевдоним): Export-AzureAsInstanceLog

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

