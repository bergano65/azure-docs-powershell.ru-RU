---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973027"
---
# Get-AzAccessToken

## SYNOPSIS
Получить необработанные маркеры доступа. При использовании ресурса ResourceUrl убедитесь, что значение соответствует текущей среде Azure. Вы можете ссылаться на значение `(Get-AzContext).Environment` .

## СИНТАКСИС

### KnownResourceTypeName (Default)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Получить маркер доступа

## ПРИМЕРЫ

### Пример 1. Получить необработанные маркеры доступа для ARM конечной точки
```powershell
PS C:\> Get-AzAccessToken
```

Получить маркер доступа конечной точки "Ресурс" для текущей учетной записи

### Пример 2. Получить необработанные маркеры доступа для конечной точки AAD Graph
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Получить маркер доступа конечной точки AAD Graph для текущей учетной записи

### Пример 3. Получить необработанные маркеры доступа для конечной точки AAD Graph
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Получить маркер доступа конечной точки AAD Graph для текущей учетной записи

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

### -ResourceTypeName
Необязательное имя типа повторного сведения, поддерживаемые значения: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Значение по умолчанию — Arm, если не указано.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
URL-адрес ресурса, для который запрашивается токен, например ' http://graph.windows.net/ .

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Необязательный ИД клиента. Используйте стандартный контекст с ид клиента, если он не указан.

```yaml
Type: System.String
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

### Нет

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
