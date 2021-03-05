---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991567"
---
# Add-AzVMAdditionalUnattendContent

## SYNOPSIS
Добавляет сведения в неотвеченный файл ответа на запрос в установке Windows.

## СИНТАКСИС

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для получения сведений в файле ответа на сведения о настройке Windows добавляется **cmdlet Add-AzVMAdditionalUnattendContent.**
Укажите дополнительные сведения в формате XML с unattend.xml 64.

## ПРИМЕРЫ

### Пример 1. Добавление содержимого в unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Первая команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в переменной $AvailabilitySet ресурса.
Вторая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Третья команда создает объект учетных данных с Get-Credential командлетом, а затем сохраняет результат в $Credential переменной.
В результате будет предложено вводить имя пользователя и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .
Четвертая команда использует командлет **Set-AzVMOperatingSystem** для настройки виртуальной машины, $VirtualMachine.
Пятая команда назначает содержимое переменной $AucContent.
Содержимое содержит пароль.
Конечная команда добавит содержимое из $AucContent в unattend.xml файл.

## PARAMETERS

### -Содержимое
Определяет содержимое в кодированном XML-формате с базой 64.
Этот cmdlet добавит содержимое в unattend.xml файл.
Содержимое XML должно быть меньше 4 КБ и должно включать корневой элемент для параметра или функции, вставляемой этим cmdlet.

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

### -SettingName
Определяет имя параметра, к которому применяется содержимое.
Допустимые значения этого параметра:
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Определяет объект виртуальной машины, который изменяет этот cmdlet.
Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzVM.](./Get-AzVM.md)
Создайте объект виртуальной машины с помощью [cmdlet New-AzVMConfig.](./New-AzVMConfig.md)

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
