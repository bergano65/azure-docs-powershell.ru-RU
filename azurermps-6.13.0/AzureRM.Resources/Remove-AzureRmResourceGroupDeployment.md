---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 19662972e115acb0e3a194e14abf3f956d39035e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562676"
---
# Remove-AzureRmResourceGroupDeployment

## КРАТКИй обзор
Удаляет развертывание группы ресурсов и связанные с ней операции.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### RemoveByResourceGroupName (по умолчанию)
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceGroupDeploymentId
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию API, поддерживаемую поставщиком ресурсов.
Вы можете выбрать версию, отличную от версии по умолчанию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -ID
Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя развертывания группы ресурсов, которую нужно удалить.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

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
Указывает имя удаляемой группы ресурсов.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmResourceGroupDeployment](./Get-AzureRmResourceGroupDeployment.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Остановить-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


