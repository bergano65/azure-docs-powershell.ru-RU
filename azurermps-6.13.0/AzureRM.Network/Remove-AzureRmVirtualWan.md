---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
ms.openlocfilehash: 1ff9eb4307c4419dd303d74f7528a8ee0d50bdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562800"
---
# Remove-AzureRmVirtualWan

## КРАТКИй обзор
Удаляет виртуальную глобальную сеть Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByVirtualWanName (по умолчанию)
```
Remove-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualWanObject
```
Remove-AzureRmVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualWanResourceId
```
Remove-AzureRmVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Удаляет виртуальную глобальную сеть Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

Этот пример создает виртуальную глобальную сеть в группе ресурсов, а затем немедленно удаляет ее. Чтобы отключить вывод запроса при удалении виртуальной глобальной сети, используйте флаг-force.

### Пример 2

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -InputObject $virtualWan -Passthru
```

Этот пример создает виртуальную глобальную сеть в группе ресурсов, а затем немедленно удаляет ее. Это удаление происходит при использовании объекта виртуальной глобальной сети, возвращенного командой New-AzureRmVirtualWan.
Чтобы отключить вывод запроса при удалении виртуальной глобальной сети, используйте флаг-force.

### Пример 3

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -ResourceId $virtualWan.Id -Passthru
```

Этот пример создает виртуальную глобальную сеть в группе ресурсов, а затем немедленно удаляет ее. Это удаление происходит при использовании идентификатора виртуального глобального ресурса, возвращенного командой New-AzureRmVirtualWan.
Чтобы отключить вывод запроса при удалении виртуальной глобальной сети, используйте флаг-force.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Не запрашивать подтверждение.

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

### -InputObject
Объект виртуальной глобальной сети, который нужно удалить.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Имя виртуальной глобальной сети.

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает объект, который представляет собой элемент, с которым вы работаете.
По умолчанию этот командлет не создает никаких выходных данных.

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

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса Azure для виртуальной глобальной сети, которую нужно удалить.

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSVirtualWan

### System. String

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
