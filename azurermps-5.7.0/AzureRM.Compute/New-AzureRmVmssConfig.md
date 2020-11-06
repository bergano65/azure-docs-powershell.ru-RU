---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561899"
---
# New-AzureRmVmssConfig

## КРАТКИй обзор
Создает объект конфигурации VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).
Для настройки объекта VMSS необходимы другие командлеты.
Ниже приведены эти командлеты.

- Set-AzureRmVmssOsProfile
- Set-AzureRmVmssStorageProfile
- Add-AzureRmVmssNetworkInterfaceConfiguration
- Add-AzureRmVmssExtension

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта конфигурации VMSS
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

В этом примере создается объект конфигурации VMSS.
Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.
Вторая команда использует командлет **New-AzureRmVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.

## ПАРАМЕТРЫ

### -BootDiagnostic
Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Расширение
Указывает объект расширения данных для VMSS.
Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssExtension** .

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
Укажите удостоверение набора масштабов виртуальной машины, если оно настроено.

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseType
Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Указывает расположение Azure, в котором создается VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterfaceConfiguration
Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.
Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** .

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsProfile
Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.
Для задания этого объекта можно использовать командлет **Set-AzureRmVmssOsProfile** .

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Превышена подготовка
Указывает, переопределяет ли командлет переVMSS.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanName
Указывает имя плана.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanProduct
Указывает продукт плана.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanPromotionCode
Указывает код продвижения плана.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanPublisher
Указывает издателя плана.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecoveryPolicyMode
Укажите политику восстановления.

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Указывает одну группу размещения.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuCapacity
Задает количество экземпляров в VMSS.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Задает размер всех экземпляров VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
Указывает уровень VMSS.

Для этого параметра допустимы следующие значения:

- Стандартная
- Базового

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageProfile
Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.
Для задания этого объекта можно использовать командлет **Set-AzureRmVmssStorageProfile** .

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Указывает теги, которые будут назначены для VMSS.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
Заданный режим перехода на виртуальные машины в наборе масштабов.

Для этого параметра допустимы следующие значения:

- Автоматически
- Вручную

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Этот командлет не создает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRmVmssOsProfile](./Set-AzureRmVmssOsProfile.md)

[Set-AzureRmVmssStorageProfile](./Set-AzureRmVmssStorageProfile.md)

[Add-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[Add-AzureRmVmssExtension](./Add-AzureRmVmssExtension.md)

[New-AzureRmVmss](./New-AzureRmVmss.md)


