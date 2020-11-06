---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560900"
---
# Get-AzureRmServiceEndpointPolicy

## КРАТКИй обзор
{Заполнение кратких описаний}

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmServiceEndpointPolicy** получает политику конечной точки службы.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

Эта команда получает политику конечной точки службы с именем ServiceEndpointPolicy1, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $policy.

### Пример 2
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

Эта команда получает список всех политик конечной точки службы в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $policyList.

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
Имя политики конечной точки службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.
Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String


## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
