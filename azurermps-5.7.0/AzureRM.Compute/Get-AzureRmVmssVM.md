---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 8d24aadd185a58472268fc4edf9ca504e7592bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561903"
---
# Get-AzureRmVmssVM

## КРАТКИй обзор
Получает свойства виртуальной машины VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### DefaultParameter (по умолчанию)
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmVmssVM** получает представление модели и экземпляр для виртуальной машины с набором масштабов виртуальных машин (VMSS).
Представление модели — это указанные пользователем свойства виртуальной машины.
Представление экземпляра — это состояние уровня экземпляра виртуальной машины.
Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение свойств виртуальной машины VMSS
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Эта команда получает свойства виртуальной машины VMSS с именем VMSS001, которая относится к группе ресурсов с именем Group001.
Так как в команде не указан параметр переключателя *InstanceView* , командлет получает представление модели виртуальной машины.

### Пример 2: получение свойств представления модели виртуальной машины VMSS
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Эта команда получает свойства виртуальной машины VMSS с именем VMSS004, которая относится к группе ресурсов с именем Group002.
Команда получает идентификатор экземпляра, хранящийся в $ID переменной, для которого требуется получить представление модели.

### Пример 3: получение свойств представления экземпляра виртуальной машины VMSS
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Эта команда получает свойства виртуальной машины VMSS с именем VMSS004, которая относится к группе ресурсов с именем Group002.
Поскольку в команде указан параметр переключателя *InstanceView* , командлет получает представление экземпляра виртуальной машины.
Команда получает идентификатор экземпляра, хранящийся в $ID переменной, для которого требуется получить представление экземпляра.

## ПАРАМЕТРЫ

### -InstanceId
Указывает идентификатор экземпляра, для которого требуется получить представление модели.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов для VMSS.

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

### -VMScaleSetName
Форель имя VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
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

### Этот командлет не создает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


