---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065624"
---
# Get-AzVMGuestPolicyStatus

## КРАТКИй обзор
Возвращает состояние политики гостевой настройки (подробно) для инициативы с типом "Гостевая конфигурация", назначенной ВМ.
Инициатива — это политика типа определения "инициатива".

## Максимальное

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

## NОПИСАНИЕ
Командлет Get-AzVMGuestPolicyStatus получает статусы политики гостевой конфигурации для инициативы типа "Гостевая конфигурация", назначенной ВМ.
Инициатива — это политика типа определения "инициатива".
Этот командлет получает состояние соответствия требованиям виртуальной машины и причины, по которым она не соответствует требованиям отдельных политик в инициативе.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Получение всех последних состояний политики настройки гостевой конфигурации для виртуальной машины.
Этот статус включает состояние соответствия виртуальной машине для каждой политики во всех инициативах типа "Конфигурация гостя", причины соответствия требованиям, время проверки соответствия требованиям, сведения о ресурсе, которые были проверены на соответствие требованиям.
Результаты включают последние статусы и не включают предыдущие исторические статусы.

### Пример 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Получение последних состояний политики настройки гостевой конфигурации по идентификатору инициативы. Состояние соответствия требованиям виртуальной машины для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия требованиям, сведения о ресурсе, которые были проверены на соответствие требованиям.
Результаты не включают в себя предыдущие состояния, они просто содержат Последнее состояние для каждой политики в инициативе.

### Пример 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Получение последних состояний политики настройки гостевой конфигурации по названию инициативы.
Состояние соответствия требованиям виртуальной машины для каждой политики в инициативе, причины соответствия требованиям, время проверки соответствия требованиям, сведения о ресурсе, которые были проверены на соответствие требованиям.
Результаты не включают в себя предыдущие состояния, они просто содержат Последнее состояние для каждой политики в инициативе.

### Пример 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Получение состояния политики гостевой настройки по ReportId.
ReportId — это свойство ReportId, которое можно найти в результатах Get-AzVMGuestPolicyStatus по имени initiativeId или инициативы (пожалуйста, ознакомьтесь с другими примерами).

## ПАРАМЕТРЫ

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
Идентификатор определения политики, в которой тип определения — инициатива, а категория — конфигурация гостя.

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
Имя политики, в которой тип определения — инициатива, а категория — конфигурация гостя

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
Идентификатор состояния политики гостевой конфигурации.
Политика, в которой тип определения — инициатива, и категория является Гостевой конфигурацией, должна быть назначена области для получения сведений о состоянии.

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
Имя ВМ.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed
## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
