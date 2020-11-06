---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 466cb31bd5e05235085fbc4f9045cf201a806e11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558556"
---
# Stop-AzureRmAutomationDscNodeConfigurationDeployment

## КРАТКИй обзор
Останавливает развертывание конфигурации узла DSC в автоматизации. Оно только останавливает текущее задание развертывания, но не отменяет уже назначенные конфигурации узла.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByJobId (по умолчанию)
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Stop-AzureRmAutomationDscNodeConfigurationDeployment** останавливает развертывание конфигурации нужной конфигурации узла (DSC) в Azure Automation. Она прекращает назначение конфигурации узла группам узлов, если они остаются назначенными, но не отменяют назначение уже назначенным узлам. Чтобы отменить регистрацию запланированного задания, используйте параметр [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) с параметром JobScheduleId для отмены назначения существующего запланированного задания.

## ИЛЛЮСТРИРУЮТ

### Пример 1: развертывание конфигурации узла Azure DSC в автоматизации
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

Указанная выше команда останавливает задание развертывания конфигурации узла DSC с переданным jobId.

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Force
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект ввода для трубопроводов

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Указывает код задания для существующего задания развертывания.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

### System. GUID

### Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment
Параметры: InputObject (ByValue)

### System. String

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Start-AzureRmAutomationDscCompilationJob](./Start-AzureRmAutomationDscCompilationJob.md)

[Import-AzureRmAutomationDscNodeConfiguration](./Import-AzureRmAutomationDscNodeConfiguration.md)

[Start-AzureRmAutomationDscNodeConfigurationDeployment](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[Get-AzureRmAutomationDscNodeConfigurationDeployment](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
