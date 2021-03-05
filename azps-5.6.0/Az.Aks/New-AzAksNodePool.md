---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 07944177b7c92ff4c515b6d9dcd01d11d3c5a888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962563"
---
# New-AzAksNodePool

## SYNOPSIS
Создайте новый пул узлов в указанном кластере.

## СИНТАКСИС

### defaultParameterSet
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ParentObjectParameterSet
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Создайте новый пул узлов в указанном кластере.

## ПРИМЕРЫ

### Создание пула узлов с параметрами по умолчанию
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### Создание контейнера Windows Server на сервере AKS
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## PARAMETERS

### -ClusterName
Имя ресурса управляемого кластера.

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterObject
Укажите объект кластера, в котором нужно создать пул узлов.

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Count
Число узлов по умолчанию для пулов узлов.

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

### -EnableAutoScaling
Следует ли включить авторе шкалу

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

### -Force
Создание пула узлов, даже если он уже существует

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

### -KubernetesVersion
Версия Кубберсетей, используемая для создания кластера.

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

### -MaxCount
Максимальное количество узлов для автоматического масштабирования

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

### -MaxPodCount
Максимальное количество pods, которые могут запускаться в узле.

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

### -MinCount
Минимальное количество узлов для автоматического масштабирования.

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

### -Name
Имя пула узлов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskSize
Число узлов по умолчанию для пулов узлов.

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

### -OsType
OsType, используемый для указания типа оси.
Выберите Linux и Windows.
Значение по умолчанию для Linux.

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

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScaleSetEvictionPolicy
ScaleSetEvictionPolicy, которая используется для указания политики разборки для набора виртуальных машин с низким приоритетом.
Значение по умолчанию для удаления.

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

### -ScaleSetPriority
ScaleSetPriority, используемое для указания приоритета набора масштаба виртуальной машины.
Значение по умолчанию ( обычный).

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

### -VmSetType
Представляет типы пула узлов.
Возможные значения: 'VirtualMachineScaleSets', 'AvailabilitySet'

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

### -VmSize
Размер виртуальной машины. Значение по умолчанию — Standard_D2_v2.

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

### -VnetSubnetID
Код подсети VNet указывает идентификатор подсети VNet.

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

### Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster

## OUTPUTS

### Microsoft.Azure.Commands.Aks.Models.PSNodePool

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
