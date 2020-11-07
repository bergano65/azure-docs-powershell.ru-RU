---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 4093e236f84d7587586ba30c8bd4653c4ba7358f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911324"
---
# Set-AzVMSqlServerExtension

## КРАТКИй обзор
Задает расширение Azure SQL Server на виртуальной машине.

## Максимальное

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzVMSqlServerExtension** задает серверное расширение AzureSQL на виртуальной машине.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка автоматических параметров исправлений на виртуальной машине
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoPatchingConfig** .
Эта команда хранит конфигурацию в переменной $AutoPatchingConfig.

Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 с помощью командлета Get-AzVM.
Команда передает этот объект в текущий командлет с помощью оператора конвейера.

Текущий командлет задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.
Команда передает виртуальную машину командлету Update-AzVM.

### Пример 2: Настройка параметров автоматического резервного копирования на виртуальной машине
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoBackupConfig** .
Эта команда хранит конфигурацию в переменной $AutoBackupConfig.

Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 и передает ее в текущий командлет.

Текущий командлет задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.
Команда передает виртуальную машину командлету Update-AzVM.

### Пример 3: отключение расширения SQL Server на виртуальной машине
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.
Команда отключает расширение виртуальной машины SQL Server на этой виртуальной машине.

### Пример 4: удаление расширения SQL Server на определенной виртуальной машине
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.
Команда удаляет расширение виртуальной машины SQL Server на этой виртуальной машине.

## ПАРАМЕТРЫ

### -AutoBackupSettings
Задает параметры автоматического резервного копирования SQL Server.
Чтобы создать объект **AutoBackupSettings** , используйте командлет New-AzureVMSqlServerAutoBackupConfig.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Задает параметры автоматического исправления SQL Server.
Чтобы создать объект **AutoPatchingSettings** , используйте командлет New-AzureVMSqlServerAutoPatchingConfig.

```yaml
Type: AutoPatchingSettings
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Указывает расположение виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя сервера SQL Server, на котором находится расширение.

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

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Указывает версию расширения SQL Server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, на которой этот командлет задает расширение SQL Server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[New-AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


