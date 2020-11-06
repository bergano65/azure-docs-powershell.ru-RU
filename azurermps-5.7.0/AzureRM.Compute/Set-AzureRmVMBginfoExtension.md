---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559156"
---
# Set-AzureRmVMBginfoExtension

## КРАТКИй обзор
Добавляет расширение BGInfo к виртуальной машине.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVMBGInfoExtension** добавляет расширение BGInfo на виртуальную машину.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление расширения BGInfo на виртуальную машину
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
Эта команда добавляет расширение BGInfo на виртуальную машину с именем ContosoVM в группе ресурсов ContosoRG.

### Пример 2: Добавление определенной версии расширения BGInfo на виртуальную машину
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

Эта команда добавляет расширение BGInfo к виртуальной машине с именем ContosoVM.
Команда определяет группу ресурсов и расположение виртуальной машины.
Команда задает имя и версию расширения.

## ПАРАМЕТРЫ

### -DisableAutoUpgradeMinorVersion
Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширение до более поздней дополнительной версии.
По умолчанию этот командлет позволяет гостевому агенту обновить расширение.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
Указывает, что расширение следует запускать с теми же открытыми или защищенными параметрами.
Значением может быть любая строка, отличающаяся от текущего значения.

Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя расширения BGInfo, которое этот командлет добавляет для виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины, на которую этот командлет добавляет расширение.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Указывает версию расширения, которое этот командлет добавляет на виртуальную машину.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, на которую этот командлет добавляет расширение BGInfo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.

Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

