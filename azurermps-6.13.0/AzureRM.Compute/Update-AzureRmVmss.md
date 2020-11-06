---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566529"
---
# Update-AzureRmVmss

## КРАТКИй обзор
Обновляет состояние VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### DefaultParameter (по умолчанию)
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Update-AzureRmVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS $LocalVMSS.

## ПАРАМЕТРЫ

### -AsJob
Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.

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

### -AutomaticOSUpgrade
Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsEnabled
Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.

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

### -CustomData
Задает строку настраиваемых данных, закодированную в формате 64.
Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.
Максимальная длина двоичного массива составляет 65535 байт.

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

### -DisableAutoRollback
Отключение автоматического отката для политики автоматического обновления ОС

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Указывает, что этот командлет отключает проверку пароля для ОС Linux.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
Указывает, включены ли на виртуальных машинах Windows в VMSS автоматическое обновление.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityId
Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.
Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Указывает тип удостоверения, используемого для набора шкал виртуальной машины.
Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.
Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.
Для этого параметра допустимы следующие значения:
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- Ничего

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceId
Указывает идентификатор ссылки на изображение.

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

### -ImageReferenceOffer
Указывает тип предложения для образа виртуальной машины (VMImage).
Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.

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

### -ImageReferencePublisher
Указывает имя издателя VMImage.
Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.

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

### -ImageReferenceSku
Указывает SKU VMImage.
Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.

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

### -ImageReferenceVersion
Указывает версию VMImage.
Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.

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

### -ImageUri
Указывает URI большого двоичного объекта для пользовательского изображения.
VMSS создает диск операционной системы в том же контейнере пользовательского образа.

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

### -LicenseType
Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.

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

### -ManagedDiskStorageAccountType
Указывает тип учетной записи хранения для управляемого диска.
Для этого параметра допустимы следующие значения:
- StandardLRS
- PremiumLRS

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

### -MaxBatchInstancePercent
Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.
Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.
Если значение не задано, оно равно 20.

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

### -MaxUnhealthyInstancePercent
Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.
Это ограничение будет проверяться перед запуском какого – либо пакета.
Если значение не задано, оно равно 20.

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

### -MaxUnhealthyUpgradedInstancePercent
Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.
Эта проверка произойдет после обновления каждого пакета.
Если это процентное значение превышено, чередующееся обновление прерывается.
Если значение не задано, оно равно 20.

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

### -OsDiskCaching
Задает режим кэширования диска операционной системы. Для этого параметра допустимы следующие значения:
- Ничего
- Чтения
- ReadWrite по умолчанию используется значение ReadWrite.
Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.
Этот параметр влияет на согласованность и производительность диска.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Превышена подготовка
Указывает, переопределяет ли командлет переVMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.
Длительность времени следует указывать в формате ISO 8601.
Значением по умолчанию является 0 секунд (PT0S).

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

### -PlanName
Указывает имя плана.

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

### -PlanProduct
Указывает продукт плана.

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

### -PlanPromotionCode
Указывает код продвижения плана.

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

### -PlanPublisher
Указывает издателя плана.

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

### -ProvisionVMAgent
Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах Windows в VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, к которой принадлежит VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Указывает одну группу размещения.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
Задает количество экземпляров в VMSS.

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

### -SkuName
Задает размер всех экземпляров VMSS.

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

### -SkuTier
Указывает уровень VMSS.
Для этого параметра допустимы следующие значения:
- Стандартная
- Базового

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

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Часовой пояс
Задает часовой пояс для операционной системы Windows.

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

### -UltraSSDEnabled
Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.
Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
Заданный режим перехода на виртуальные машины в наборе масштабов.
Для этого параметра допустимы следующие значения:
- Автоматически
- Вручную
- За

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Указывает локальный объект VMSS.
Чтобы получить объект VMSS, используйте командлет Get-AzureRmVmss.
Этот объект виртуальной машины включает обновленное состояние для VMSS.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Указывает имя VMSS, создаваемого этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet
Параметры: VirtualMachineScaleSet (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[New-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restarting-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Остановить-AzureRmVmss](./Stop-AzureRmVmss.md)


