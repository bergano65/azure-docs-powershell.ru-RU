---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395119"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
Возвращает статусы политики настройки гостей (подробный) для инициативы типа "Гостевая конфигурация", которая назначена VM.
Инициатива — это политика типа определения "Инициатива".

## СИНТАКСИС

### VmScope (по умолчанию)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Этот Get-AzVMGuestPolicyStatus получает состояние политики настройки гостей для инициативы типа "Гостевая конфигурация", которая назначена VM.
Инициатива — это политика определения типа "Инициатива".
Этот cmdlet получает статус соответствия требованиям для VM-управления и причины, по которым он не соответствует отдельным политикам в инициативе.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Получите все последние состояния политики настройки гостей для VM.
Состояние включает состояние соответствия VM для каждой политики всеми инициативами типа "Гостевая конфигурация", причины соответствия требованиям, время проверки соответствия, сведения о ресурсах, которые были проверены на соответствие требованиям.
Результаты включают последние состояния, но не включают предыдущие исторические состояния.

### Пример 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Получите последние состояния политики гостевой конфигурации по ид инициативной конфигурации. Состояние включает состояние соответствия VM для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия, сведения о ресурсах, которые были проверены на соответствие требованиям.
В результатах не содержатся ранее созданные состояния, а только последние состояния каждой политики в инициативе.

### Пример 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

По названиям инициатив вы получаете последние состояния политики настройки гостей.
Состояние включает состояние соответствия VM для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия, сведения о ресурсах, которые были проверены на соответствие требованиям.
В результатах не содержатся ранее созданные состояния, а только последние состояния каждой политики в инициативе.

### Пример 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Получите состояние политики настройки гостей по ReportId.
ReportId — это свойство ReportId, которое можно найти в результатах поиска по Get-AzVMGuestPolicyStatus initiativeId или initiative name (см. другие примеры).

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

### -InitiativeId
Определение ИД политики, в которой тип определения — Initiative, а категория — Guest Configuration

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
Имя политики, для которой тип определения — Initiative, а категория — Guest Configuration

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId
ИД состояния политики "Гостевая конфигурация".
Политика, в которой тип определения — Initiative, а категория — Guest Configuration, должна быть назначена области для получения состояния.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Имя VM.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
## OUTPUTS

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
