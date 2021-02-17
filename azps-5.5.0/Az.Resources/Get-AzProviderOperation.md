---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220545"
---
# Get-AzProviderOperation

## SYNOPSIS
Получает операции для поставщика ресурсов Azure, защищаемые с помощью Azure RBAC.

## СИНТАКСИС

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Служба Get-AzProviderOperation получает операции, которые поставщика ресурсов Azure 2010 2016.
Операции можно создавать для создания настраиваемой роли в Azure RBAC.
Команда принимается в качестве входной строки поиска операций (с возможными поддиавными знаками) символов, которая определяет отображаемую информацию *об операциях. Используйте Get-AzProviderOperation * для получения всех операций для всех поставщиков ресурсов Azure. Используйте Get-AzProviderOperation Microsoft.Compute/,* чтобы получить все операции поставщика ресурсов Microsoft.Compute.

## ПРИМЕРЫ

### Пример 1. Получить все действия для всех поставщиков
```powershell
PS C:\> Get-AzProviderOperation *
```

### Пример 2. Получить действия для конкретного поставщика ресурсов
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Пример 3. Получить все действия, которые можно выполнять на виртуальных машинах
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETERS

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

### -OperationSearchString
Строка поиска операции (с возможными поддиавными знаками (*)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## ПРИМЕЧАНИЯ
Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## СВЯЗАННЫЕ ССЫЛКИ
