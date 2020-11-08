---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248275"
---
# Disable-AzDataCollection

## КРАТКИй обзор
Изменяют сбор данных для улучшения командлетов PowerShell для Azure. Данные собираются по умолчанию, если только вы не выберете явное согласие.

## Максимальное

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ

Этот `Disable-AzDataCollection` командлет используется, чтобы отказаться от сбора данных. Azure PowerShell автоматически собирает данные телеметрии по умолчанию. Чтобы отключить сбор данных, необходимо явно отказаться от него. Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для улучшения работы Azure PowerShell. Microsoft Azure PowerShell не собирают конфиденциальные или личные данные. Если вы ранее выделились, выполните `Enable-AzDataCollection` командлет, чтобы повторно включить сбор данных для текущего пользователя на текущем компьютере.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Отключение сбора данных для текущего пользователя

В следующем примере показано, как отключить сбор данных для текущего пользователя.

```powershell
Disable-AzDataCollection
```

## ПАРАМЕТРЫ

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

### -Confirm

Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### System. void

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
