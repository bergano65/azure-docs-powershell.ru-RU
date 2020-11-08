---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065135"
---
# Get-AzPowerBIWorkspaceCollection

## КРАТКИй обзор
Получение коллекций рабочих областей Power BI.

## Максимальное

### ResourceGroupParameterSet
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WorkspaceCollectionNameParameterSet
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzPowerBIWorkspaceCollection** получает наборы рабочих областей Power BI в подписке и группе ресурсов Azure, а также по имени коллекции.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех коллекций рабочих областей в группе ресурсов
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

Эта команда возвращает коллекции рабочих областей, которые принадлежат группе ресурсов с именем ResourceGroup17.

### Пример 2: получение коллекции рабочих областей с использованием ее имени
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

Эта команда получает набор рабочих областей с именем WCN11 в указанной группе ресурсов.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, из которой этот командлет получает коллекции рабочих областей.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceCollectionName
Указывает имя коллекции рабочих областей Power BI, которую этот командлет получает.

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzPowerBIWorkspaceCollection](./New-AzPowerBIWorkspaceCollection.md)

[Remove-AzPowerBIWorkspaceCollection](./Remove-AzPowerBIWorkspaceCollection.md)


