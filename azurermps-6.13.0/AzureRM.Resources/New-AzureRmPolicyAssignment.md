---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 616b75b4bdc5dab9f02bb1fc295effefc0e728be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556511"
---
# New-AzureRmPolicyAssignment

## КРАТКИй обзор
Создание назначения политики.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### DefaultParameterSet (по умолчанию)
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterObjectParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterStringParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterObjectParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterStringParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmPolicyAssignment** создает назначение политики.
Укажите политику и область действия.

## ИЛЛЮСТРИРУЮТ

### Пример 1: назначение политики на уровне группы ресурсов
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup и сохраняет его в переменной $ResourceGroup.
Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzureRmPolicyDefinition и сохраняет его в переменной $Policy.
Последняя команда назначает политику в $Policy на уровне группы ресурсов, определяемой свойством **ResourceId** $ResourceGroup.

### Пример 2: назначение политики на уровне группы ресурсов с объектом параметра политики
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.
Команда сохраняет этот объект в переменной $ResourceGroup.
Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzureRmPolicyDefinition.
Команда сохраняет этот объект в переменной $Policy.
Третья и четвертая команды создают объект, содержащий все регионы Azure с именем "Восток".
Команды хранят этот объект в переменной $AllowedLocations.
Последняя команда назначает политику в $Policy на уровне группы ресурсов, используя объект параметра политики в $AllowedLocations.
Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.

### Пример 3: назначение политики на уровне группы ресурсов с помощью файла параметров политики
Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup и сохраняет его в переменной $ResourceGroup.
Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzureRmPolicyDefinition и сохраняет его в переменной $Policy.
Последняя команда назначает политику в $Policy в группе ресурсов, определяемой свойством **ResourceId** $ResourceGroup с помощью файла параметров политики AllowedLocations.json из локального рабочего каталога.

### Пример 4: назначение политики с управляемым удостоверением
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup и сохраняет его в переменной $ResourceGroup.
Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzureRmPolicyDefinition и сохраняет его в переменной $Policy.
Последняя команда назначает политику в $Policy группе ресурсов. Управляемое удостоверение создается автоматически и назначается назначению политики.

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию используемого API поставщика ресурсов.
Если вы не укажете версию, этот командлет использует последнюю доступную версию.

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

### -AssignIdentity
Создание и назначение удостоверения Azure Active Directory для этого назначения политики. Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists". При назначении удостоверения требуется указать расположение.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Описание
Описание назначения политики

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

### -DisplayName
Задает отображаемое имя для назначения политики.

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

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.
Для этого параметра допустимы следующие значения:
- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Расположение удостоверения ресурса для назначения политики. Это необходимо, если используется параметр-AssignIdentity.

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

### -Metadata
Метаданные для нового назначения политики. Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.

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

### -Name (имя)
Задает имя для назначения политики.

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

### -NotScope
Область "не для назначения политики".

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinition
Указывает политику как объект **PsPolicyDefinition** , который содержит правило политики.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameter
Путь к файлу параметра политики или строка параметра политики.

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameterObject
Объект параметра политики.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicySetDefinition
Объект определения параметра политики.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Указывает область, в которой нужно назначить политику.
Например, чтобы назначить политику группе ресурсов, укажите следующее: `/subscriptions/` `/resourcegroups/` имя группы ресурсов для идентификатора подписки

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

### -SKU
Хэш-таблица, представляющая свойства SKU. По умолчанию используется бесплатная SKU со значениями: `@{Name = 'A0'; Tier = 'Free'}` . Чтобы использовать стандартную SKU, используйте значения: `@{Name = 'A1'; Tier = 'Standard'}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[Get-AzureRmPolicyAssignment](./Get-AzureRmPolicyAssignment.md)

[Remove-AzureRmPolicyAssignment](./Remove-AzureRmPolicyAssignment.md)

[Set-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)


