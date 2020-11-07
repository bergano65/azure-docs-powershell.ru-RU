---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 2a1dbf5eea7f772a7819ed341a681adc24134225
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914189"
---
# Set-AzureRmVMSqlServerExtension

## КРАТКИй обзор
Задает расширение Azure SQL Server на виртуальной машине.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVMSqlServerExtension** задает серверное расширение AzureSQL на виртуальной машине.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка автоматических параметров исправлений на виртуальной машине
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoPatchingConfig** .
Эта команда хранит конфигурацию в переменной $AutoPatchingConfig.

Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 с помощью командлета Get-AzureRmVM.
Команда передает этот объект в текущий командлет с помощью оператора конвейера.

Текущий командлет задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.
Команда передает виртуальную машину командлету Update-AzureRmVM.

### Пример 2: Настройка параметров автоматического резервного копирования на виртуальной машине
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoBackupConfig** .
Эта команда хранит конфигурацию в переменной $AutoBackupConfig.

Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 и передает ее в текущий командлет.

Текущий командлет задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.
Команда передает виртуальную машину командлету Update-AzureRmVM.

### Пример 3: отключение расширения SQL Server на виртуальной машине
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.
Команда отключает расширение виртуальной машины SQL Server на этой виртуальной машине.

### Пример 4: удаление расширения SQL Server на определенной виртуальной машине
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMSqlServerExtension](./Get-AzureRMVMSqlServerExtension.md)





[Remove-AzureRmVMSqlServerExtension](./Remove-AzureRMVMSqlServerExtension.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


