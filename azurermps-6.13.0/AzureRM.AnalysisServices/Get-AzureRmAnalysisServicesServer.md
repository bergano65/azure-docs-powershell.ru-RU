---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: efd4c4770bb9a2628530f476d44e9774534ceee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563195"
---
# Get-AzureRmAnalysisServicesServer

## КРАТКИй обзор
Получает сведения о сервере служб Analysis Services.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmAnalysisServicesServer получает сведения о сервере служб Analysis Services.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

Эта команда получает все серверы служб аналитики Azure в группе ресурсов с именем ResourceGroup03.

### Пример 2: получение сервера
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

Эта команда получает сервер служб аналитики Azure с именем TestServer в группе ресурсов с именем ResourceGroup03.

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
Имя сервера служб Analysis Services

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов Azure, к которой принадлежит сервер

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer

## Пуск
Alias (псевдоним): Get-AzureAs

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmAnalysisServicesServer ](./New-AzureRmAnalysisServicesServer .md)

[Remove-AzureRmAnalysisServicesServer ](./Remove-AzureRmAnalysisServicesServer .md)
