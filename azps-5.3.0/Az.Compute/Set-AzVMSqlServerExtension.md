---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519444"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Задает расширение Azure SQL Server на виртуальной машине.

## СИНТАКСИС

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для виртуальной машины задается расширение AzureSQL Server с использованием cmdlet **Set-AzVMSqlServerExtension.**

## ПРИМЕРЫ

### Пример 1. Настройка параметров автоматического исправления на виртуальной машине
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Первая команда создает объект конфигурации с помощью командлета **New-AzVMSqlServerAutoPatchingConfig.**
Команда сохраняет конфигурацию в переменной $AutoPatchingConfig.
Вторая команда получает виртуальную машину VirtualMachine11 в службе Service02 с Get-AzVM командлетом.
Эта команда передает этот объект текущему командлету с помощью оператора конвейера.
Текущий cmdlet задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.
Эта команда передает виртуальную машину к Update-AzVM командлету.

### Пример 2. Настройка параметров автоматического резервного копирования на виртуальной машине
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Первая команда создает объект конфигурации с помощью командлета **New-AzVMSqlServerAutoBackupConfig.**
Команда сохраняет конфигурацию в переменной $AutoBackupConfig.
Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе Service02 и передает ее текущему командлету.
Текущий cmdlet задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.
Эта команда передает виртуальную машину к Update-AzVM командлету.

### Пример 3. Отключение расширения SQL Server на виртуальной машине
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Эта команда получает виртуальную машину с именем VirtualMachine08 в службе Service03 и передает ее текущему командлету.
Эта команда отключает расширение SQL Server на этой виртуальной машине.

### Пример 4. Удалить расширение SQL Server на определенной виртуальной машине
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Эта команда получает виртуальную машину с именем VirtualMachine08 в службе Service03 и передает ее текущему командлету.
Эта команда выгрузит расширение SQL Server на этой виртуальной машине.

## PARAMETERS

### -AutoBackupSettings
Параметры автоматического SQL Server параметры резервного копирования.
Чтобы создать объект **AutoBackupSettings,** используйте New-AzVMSqlServerAutoBackupConfig..

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Определяет параметры автоматического SQL Server исправлений.
Чтобы создать объект **AutoPatchingSettings,** используйте New-AzVMSqlServerAutoPatchingConfig..

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Определяет расположение виртуальной машины.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Указывает имя имени SQL Server расширения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Определяет версию расширения SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, на которой этот SQL Server расширения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

### Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


