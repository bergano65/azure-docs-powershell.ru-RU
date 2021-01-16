---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326776"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
Удаляет план приложения с функцией.

## СИНТАКСИС

### ByName (по умолчанию)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Удаляет план приложения с функцией.

## ПРИМЕРЫ

### Пример 1. Получите план приложения функции по имени и удалите его.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Эта команда получает план приложения функции по имени и удаляет его.

### Пример 2. Удаление плана приложения функции по имени.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Эта команда удаляет план приложения функции по имени.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Позволяет удалить план приложения с функцией, не запросив подтверждение.

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

### -InputObject
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя приложения функции.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает "Истина" в случае успешного достижения команды.

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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД подписки Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


<IAppServicePlan>INPUTOBJECT: 
  - `Location <String>`: Расположение ресурса.
  - `[Kind <String>]`: Тип ресурса.
  - `[Tag <IResourceTags>]`: теги ресурсов.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[Capacity <Int32?>]`: Текущее количество экземпляров, которые назначены ресурсу.
  - `[FreeOfferExpirationTime <DateTime?>]`. Время истечения срока действия бесплатного предложения фермы серверов.
  - `[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.
  - `[HyperV <Boolean?>]`: Если это план обслуживания контейнера Hyper-V, <code>true</code> <code>false</code> в противном случае.
  - `[IsSpot <Boolean?>]`. Если этот план служб приложения является владельцем <code>true</code> точековых экземпляров.
  - `[IsXenon <Boolean?>]`: Устарело: план обслуживания контейнера Hyper-V, в <code>true</code> <code>false</code> противном случае.
  - `[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана обслуживания приложения ВадимScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Если приложения, которые назначены этому плану обслуживания приложений, <code>true</code> можно масштабировать независимо друг от друга.         Если приложения, которые назначены этому плану обслуживания приложений, будут масштабироваться во всех <code>false</code> его экземплярах.
  - `[Reserved <Boolean?>]`. Если вы планируете службу приложения <code>true</code> Linux, <code>false</code> в противном случае.
  - `[SkuCapability <ICapability[]>]`. Возможности SKU, например, включен ли диспетчер трафика?
    - `[Name <String>]`: Имя возможности SKU.
    - `[Reason <String>]`: Причина возможности SKU.
    - `[Value <String>]`: значение возможности SKU.
  - `[SkuCapacityDefault <Int32?>]`: Число сотрудников по умолчанию для этого плана обслуживания приложений.
  - `[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана обслуживания приложений.
  - `[SkuCapacityMinimum <Int32?>]`: Минимальное количество сотрудников для этого SKU плана обслуживания приложений.
  - `[SkuCapacityScaleType <String>]`: Доступны масштаб конфигурации для плана службы приложений.
  - `[SkuFamily <String>]`: семейный код SKU ресурса.
  - `[SkuLocation <String[]>]`: Местоположения SKU.
  - `[SkuName <String>]`: Имя SKU ресурса.
  - `[SkuSize <String>]`: Заданный размер SKU ресурса.
  - `[SkuTier <String>]`: уровень обслуживания SKU ресурса.
  - `[SpotExpirationTime <DateTime?>]`Время истечения срока действия фермы серверов. Допустимо только в том случае, если это ферма точественных серверов.
  - `[TargetWorkerCount <Int32?>]`: количество масштабируемых сотрудников.
  - `[TargetWorkerSizeId <Int32?>]`: ИД размера масштабируемой работой.
  - `[WorkerTierName <String>]`: уровень целевого сотрудника, который назначен плану службы приложений.

## СВЯЗАННЫЕ ССЫЛКИ

