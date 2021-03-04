---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989148"
---
# Get-AzPolicyMetadata

## SYNOPSIS
Ресурсы по метаданным политики

## СИНТАКСИС

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Get-AzPolicyRemediation** можно получить все ресурсы метаданных политики или определенный ресурс метаданных политики.

## ПРИМЕРЫ

### Пример 1. Получить все ресурсы метаданных политики
```powershell
PS C:\> Get-AzPolicyMetadata
```

Эта команда получает все ресурсы метаданных политики.

### Пример 2. Получить набор из 10 ресурсов метаданных политики
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Эта команда получает набор из 10 ресурсов метаданных политики.

### Пример 3. Получить один ресурс метаданных политики с именем ACF1348
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Эта команда получает один ресурс метаданных политики с именем ACF1348.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Name
Название ресурса.

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

### -Top
Максимальное количество возвращаемых ресурсов метаданных политики.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
