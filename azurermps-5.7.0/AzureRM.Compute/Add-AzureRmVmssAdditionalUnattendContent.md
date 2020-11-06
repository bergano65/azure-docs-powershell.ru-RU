---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561919"
---
# Add-AzureRmVmssAdditionalUnattendContent

## КРАТКИй обзор
Добавляет сведения в файл ответов для автоматической настройки Windows.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmVmssAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление сведений в файл ответов для автоматической установки Windows
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

Эта команда добавляет данные в файл ответов для автоматической установки Windows.

## ПАРАМЕТРЫ

### -ComponentName
Указывает имя компонента, для которого нужно настроить добавленное содержимое.
Единственным допустимым значением является параметр Microsoft-Windows-Shell-Setup.

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Содержимое
Задает содержимое в формате XML, которое добавляется в файл unattend.xml для указанного пути и компонента.

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

### -PassName
Указывает имя прохода, к которому применяется содержимое.
Единственным допустимым значением является значение oobeSystem.

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

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
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Укажите объект для **установления масштаба** виртуальной машины.
Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
