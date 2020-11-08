---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244942"
---
# Remove-AzFunctionAppPlan

## КРАТКИй обзор
Удаляет план приложения функции.

## Максимальное

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

## NОПИСАНИЕ
Удаляет план приложения функции.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение плана приложения функции по имени и его удаление.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Эта команда получает план приложения функции по имени и удаляет его.

### Пример 2: Удаление плана приложения функции по имени.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Эта команда удаляет план приложения функции по имени.

## ПАРАМЕТРЫ

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
Принудительное удаление плана приложения функции без запроса на подтверждение командлета.

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
Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.

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

### -Name (имя)
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
Возвращает значение истина, если команда выполнена успешно.

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
Идентификатор подписки Azure.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. IAppServicePlan

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

СВЯЗЫВАЮТ

СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ

Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Расположение ресурса.
  - `[Kind <String>]`: Типа ресурса.
  - `[Tag <IResourceTags>]`: Теги ресурсов.
    - `[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[Capacity <Int32?>]`: Текущее количество экземпляров, назначенных ресурсу.
  - `[FreeOfferExpirationTime <DateTime?>]`: Время истечения срока действия бесплатного предложения фермы серверов.
  - `[HostingEnvironmentProfileId <String>]`: Идентификатор ресурса среды службы приложений.
  - `[HyperV <Boolean?>]`: <code>true</code> В противном случае, если вы хотите, чтобы контейнеры службы приложений Hyper-V <code>false</code> .
  - `[IsSpot <Boolean?>]`: Если <code>true</code> , этот план служб приложений владеет плашечными экземплярами.
  - `[IsXenon <Boolean?>]`: Устаревший: Если в качестве контейнера службы приложений для контейнеров Hyper-V — <code>true</code> <code>false</code> в противном случае.
  - `[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана служб приложений ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Если <code>true</code> приложения, назначенные для этого плана служб приложений, можно масштабировать независимо друг от друга.         Если <code>false</code> приложения, назначенные для этого плана служб приложений, будут масштабироваться во всех экземплярах плана.
  - `[Reserved <Boolean?>]`: Если план служб приложений для <code>true</code> Linux <code>false</code> в противном случае.
  - `[SkuCapability <ICapability[]>]`: Возможности SKU, например, включены ли диспетчер трафика?
    - `[Name <String>]`: Название возможности SKU.
    - `[Reason <String>]`: Причина возможности SKU.
    - `[Value <String>]`: Значение возможности SKU.
  - `[SkuCapacityDefault <Int32?>]`: Количество рабочих процессов по умолчанию для этого плана служб приложений SKU.
  - `[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана служб приложений SKU.
  - `[SkuCapacityMinimum <Int32?>]`: Минимальное количество рабочих процессов для этого плана служб приложений SKU.
  - `[SkuCapacityScaleType <String>]`: Доступные конфигурации масштабирования для плана служб приложений.
  - `[SkuFamily <String>]`: Код семейства SKU ресурса.
  - `[SkuLocation <String[]>]`: Расположение SKU.
  - `[SkuName <String>]`: Имя SKU ресурса.
  - `[SkuSize <String>]`: Указатель размера SKU ресурса.
  - `[SkuTier <String>]`: Уровень обслуживания SKU ресурса.
  - `[SpotExpirationTime <DateTime?>]`: Время истечения срока действия фермы серверов. Действует только в том случае, если это ферма серверов с плашечными серверами.
  - `[TargetWorkerCount <Int32?>]`: Масштабирование количества рабочих процессов.
  - `[TargetWorkerSizeId <Int32?>]`: Масштабирование кода размера рабочего процесса.
  - `[WorkerTierName <String>]`: Целевой рабочий уровень, назначенный плану служб приложений.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

