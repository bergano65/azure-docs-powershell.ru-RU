---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: b5676217de980aed8581a4a1e5a5ab103c86e753
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104714647"
---
# Set-AzVmssOsProfile

## SYNOPSIS
Задает свойства профиля операционной системы VMSS.

## СИНТАКСИС

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для свойства профиля виртуальной машины **Set-AzVmssOsProfile** задаются свойства профиля виртуальной машины (Scale Set).

## ПРИМЕРЫ

### Пример 1. Настройка свойств профиля операционной системы для VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Эта команда задает свойства профиля операционной системы для виртуальных машин, которые относятся к VMSS с именем ContosoVMSS.
Эта команда задает префикс имени компьютера для всех экземпляров виртуальной машины в VMSS для проверки и задает имя пользователя и пароль администратора.

## PARAMETERS

### -AdditionalUnattendContent
Определяет объект несмежного содержимого.
С помощью Add-AzVMAdditionalUnattendContent можно создать объект.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
Пароль администратора, который будет применяться для всех экземпляров виртуальной машины в VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
Указывает имя учетной записи администратора, которая будет применяться для всех экземпляров виртуальной машины в VMSS. <br>
**Ограничение только для Windows:** Не может закончиться \" .\" <br>
**Деостановимые значения** \" \"администратор, \" \" администратор, \" \" пользователь, \" \" пользователь1, \" \" проверка, \" \" пользователь2, \" \" тест1, \" \" пользователь3, \" \" администратор1, \" \" 1, \" 123, \" a , \" \" \" actuser, \" \" adm, \" \" \" admin2, \" aspnet, aspnet, \" \" \" backup, \" \" \" \" \" console, david, \" guest, \" \" \" \" owner, \" \" owner, root, \" \" server, \" sql, \" support , \" \" \" \" support_388945a0, \" sys, \" \" test2 , \" \" \" test3, \" \" user4, \" user5 \" . <br>
**Минимальная длина (Linux):** 1 знак <br>
**Максимальная длина (Linux):** 64 знака <br>
**Максимальная длина (Windows):** 20 символов  <br>
<li> Корневой доступ к Linux VM см. в этом видеоролике об использовании корневых привилегий на виртуальных машинах [Linux в Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> Список встроенных пользователей системы на Linux, которые не следует использовать в этом поле, см. в поле "Выбор имен пользователей [для Linux" в Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerNamePrefix
Указывает префикс имени компьютера для всех экземпляров виртуальной машины в VMSS.
Имена компьютеров должны иметь длину от 1 до 15 знаков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Указывает строку пользовательских данных с кодом базы 64.
Он декодироваться в двоичный массив, сохраненный в файле на виртуальной машине.
Максимальная длина двоичного массива составляет 65 535 тол. <br>
Чтобы узнать, как использовать cloud-init для своего VM-решения, см. в этой теме использование cloud-init для настройки [VM-решения Linux во](/azure/virtual-machines/linux/tutorial-automate-vm-deployment)время создания.

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

### -LinuxConfigurationDisablePasswordAuthentication
Указывает на то, что этот cmdlet отключает проверку подлинности паролем.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
Указывает, Windows Remote Management (WinRM).
Это позволит использовать удаленные Windows PowerShell.
Для создания Add-AzVmssWinRMListener можно использовать Add-AzVmssWinRMListener.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
Указывает объект открытого ключа Secure Shell (SSH).
Для создания объекта Add-AzVMSshPublicKey можно использовать Add-AzVMSshPublicKey.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Секретная
Определяет секрет объекта, который содержит ссылки на сертификаты, которые нужно разместить на виртуальной машине.
С помощью Add-AzVmssSecret можно создать объект секретов.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Определяет часовой пояс виртуальной машины. Например, по \" тихоокеанскому \" времени. <br>
Возможные значения могут [быть](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Указывает объект VMSS.
Для создания объекта New-AzVmssConfig можно использовать New-AzVmssConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Указывает, включены ли на виртуальных машинах виртуальные машины для автоматического обновления.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Указывает на то, следует ли заказать агент виртуальной машины на виртуальных машинах в VMSS.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

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

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]

### Microsoft.Azure.Management.Compute.Models.WinRMListener[]

### Microsoft.Azure.Management.Compute.Models.SshPublicKey[]

### Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


