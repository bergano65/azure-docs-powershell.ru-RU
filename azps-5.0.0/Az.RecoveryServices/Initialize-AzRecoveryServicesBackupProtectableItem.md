---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 7d481008fad138e392b73f88cc36318c3948fbf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316076"
---
# Initialize-AzRecoveryServicesBackupProtectableItem

## КРАТКИй обзор
Эта команда запускает обнаружение незащищенных элементов заданного типа рабочей нагрузки в заданном контейнере. Если приложение DB не защищено автоматически, используйте эту команду, чтобы найти новый DBs, когда они будут добавлены, и продолжите их защиту.

## Максимальное

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет зазапрос для определенных рабочих нагрузок в контейнере. Это вызывает операцию, которая создает защищенные элементы.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

Командлет выполняет операцию обнаружения для новых защищенных элементов.

### Пример 2

Эта команда запускает обнаружение незащищенных элементов заданного типа рабочей нагрузки в заданном контейнере. (автоматически сформированные)

```powershell <!-- Aladdin Generated Example --> 
Initialize-AzRecoveryServicesBackupProtectableItem -Container $Cont[0] -VaultId $vault.ID -WorkloadType AzureVM
```

## ПАРАМЕТРЫ

### -Container
Контейнер, в котором находится элемент

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -PassThru
Возвращает контейнер, в котором инициируется обнаружение.

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

### -VaultId
Идентификатор ARM хранилища служб восстановления.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkloadType
Тип рабочей нагрузки ресурса. Текущие поддерживаемые значения — AzureVM, WindowsServer, AzureFiles, MSSQL

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
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

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase
System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
