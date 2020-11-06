---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559864"
---
# New-AzureRmDataLakeAnalyticsComputePolicy

## КРАТКИй обзор
Создает правило политики COMPUTE Data Lake Analytics для определенной сущности AAD.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
**Новый параметр-AzureRmDataLakeAnalyticsComputePolicy** создает указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание политики вычислений с одним правилом
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla" для пользователя с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3", гарантирующий, что он не сможет отправлять задания с более чем 5 параллелизмом.

### Пример 2: Создание политики вычислений с обоими наборами правил
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla" для пользователя с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3", гарантирующий, что он не сможет отправлять задания с более чем 5 параллелизмом или с более низким приоритетом, чем 100

## ПАРАМЕТРЫ

### -Account (учетная запись)
Имя учетной записи, в которую нужно добавить политику вычисления.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxDegreeOfParallelismPerJob
Максимальная поддерживаемая степень параллелизма для задания в этой политике.
Необходимо указать значение, MinPriorityPerJob или оба параметра.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinPriorityPerJob
Минимальный поддерживаемый приоритет для задания в этой политике.
Необходимо указать значение, MaxDegreeOfParallelismPerJob или оба параметра.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Имя создаваемой политики вычислений.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Идентификатор объекта Azure Active Directory для пользователя или группы, к которой применяется политика.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectType
Тип объекта Azure Active Directory для переданного идентификатора объекта.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которой есть учетная запись.
Необязательный и пытается выяснить, не было ли оно указано.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String
System. GUID System. Int32

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

