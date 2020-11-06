---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565556"
---
# Remove-AzureRmVmss

## КРАТКИй обзор
Удаление VMSS или виртуальной машины, которая находится в VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmVmss** удаляет из Azure (VMSS) установленный параметр "виртуальная машина".
Этот командлет также можно использовать для удаления определенной виртуальной машины в VMSS.
Вы можете использовать параметр *InstanceId* для удаления определенной виртуальной машины в VMSS.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление VMSS
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

Эта команда удаляет VMSS с именем VMScaleSet001, который относится к группе ресурсов с именем Group001.

### Пример 2: Удаление виртуальной машины из VMSS
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

Эта команда удаляет виртуальную машину с ИДЕНТИФИКАТОРом 3 из VMSS с именем VMScaleSet002, которая относится к группе ресурсов с именем Group002.

## ПАРАМЕТРЫ

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо запустить.
Например: `-InstanceId "0", "3"`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, к которой относится VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Форель имя VMSS, которое удаляет этот командлет.
Если вы укажете параметр *InstanceId* , командлет удалит указанную виртуальную машину из VMSS с именем, указанным в этом параметре.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.
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

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[New-AzureRmVmss](./New-AzureRmVmss.md)

[Restarting-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Остановить-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


