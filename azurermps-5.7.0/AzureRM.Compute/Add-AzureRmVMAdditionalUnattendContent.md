---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563724"
---
# Add-AzureRmVMAdditionalUnattendContent

## КРАТКИй обзор
Добавляет сведения в файл ответов для автоматической настройки Windows.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmVMAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.
Укажите дополнительные данные в формате Base 64 Encoded. XML, которые этот командлет добавляет в файл unattend.xml.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление содержимого в unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.

Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.
Команда назначает имя и размер виртуальной машине.
Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.

Третья команда создает объект учетных данных с помощью командлета Get-Credential и сохраняет результат в переменной $Credential.
В командной строке будет предложено ввести имя пользователя и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

Четвертая команда использует командлет **Set-AzureRmVMOperatingSystem** для настройки виртуальной машины, хранящейся в $VirtualMachine.

Пятая команда назначает содержимое переменной $AucContent.
Содержимое включает пароль.

Последняя команда добавляет содержимое, хранящееся в $AucContent, в файл unattend.xml.

## ПАРАМЕТРЫ

### -Содержимое
Задает базовое содержимое в формате XML в кодировке 64.
Этот командлет добавляет содержимое в файл unattend.xml.
Содержимое XML должно быть меньше 4 КБ и должно включать корневой элемент для параметра или функции, вставляемой этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SettingName
Указывает имя параметра, к которому применяется содержимое.
Для этого параметра допустимы следующие значения:

- FirstLogonCommands
- Автоматический вход

```yaml
Type: SettingNames
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
Указывает объект виртуальной машины, измененный этим командлетом.
Чтобы получить объект виртуальной машины, используйте командлет [Get-AzureRmVM](./Get-AzureRmVM.md) .
Создайте объект виртуальной машины с помощью командлета [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
