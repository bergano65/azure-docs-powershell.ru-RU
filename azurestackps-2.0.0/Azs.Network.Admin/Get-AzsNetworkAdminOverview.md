---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910498"
---
# Get-AzsNetworkAdminOverview

## КРАТКИй обзор
Получите общие сведения о состоянии поставщика сетевых ресурсов.

## Максимальное

### Get (по умолчанию)
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Получите общие сведения о состоянии поставщика сетевых ресурсов.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



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

### -InputObject
Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -SubscriptionId
Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.
Идентификатор подписки образует часть URI для каждого вызова службы.

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. INetworkAdminIdentity

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IAdminOverview



## Пуск

Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.

INPUTOBJECT <INetworkAdminIdentity> : параметр Identity
  - `[Id <String>]`: Путь к удостоверению ресурса
  - `[Location <String>]`: Расположение ресурса.
  - `[ResourceName <String>]`: Имя ресурса.
  - `[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

