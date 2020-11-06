---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 6fa6b5b9bd7d73c0a2f5ea42b7878e9ce00cf6ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570292"
---
# Get-AzureRmAutomationDscNode

## КРАТКИй обзор
Возвращает узлы DSC из автоматизации.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByAll (по умолчанию)
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfiguration
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByConfiguration
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmAutomationDscNode** получает узлы точек доступа к требуемому состоянию (DSC) ТД из Azure Automation.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех узлов DSC
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Эта команда получает метаданные для всех узлов DSC в учетной записи автоматизации с именем Contoso17.

### Пример 2: получение всех узлов DSC для конфигурации DSC
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Эта команда получает метаданные для всех узлов DSC в учетной записи автоматизации с именем Contoso17, сопоставленными с конфигурацией узла DSC, созданной с помощью конфигурации DSC ContosoConfiguration.

### Пример 3: получение узла DSC по ИДЕНТИФИКАТОРу
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Эта команда получает метаданные на узле DSC с указанным ИДЕНТИФИКАТОРом в учетной записи автоматизации с именем Contoso17.

### Пример 4: получение узла DSC по имени
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

Эта команда получает метаданные на узле DSC с именем Computer14 в учетной записи автоматизации с именем Contoso17.

### Пример 5: получение всех узлов DSC, сопоставленных с конфигурацией узла DSC
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

Эта команда получает метаданные всех узлов DSC в учетной записи автоматизации с именем Contoso17, сопоставленными с конфигурацией узла DSC с именем ContosoConfiguration...

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации, содержащей узлы DSC, которые получает этот командлет.

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

### -ConfigurationName
Указывает имя конфигурации DSC.
Этот командлет получает узлы DSC, соответствующие конфигурациям узлов, созданным из конфигурации, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: ByConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает уникальный идентификатор узла DSC, который получает этот командлет.

```yaml
Type: Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя узла DSC, который получает этот командлет.

```yaml
Type: String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeConfigurationName
Указывает имя конфигурации узла, которую получает этот командлет.

```yaml
Type: String
Parameter Sets: ByNodeConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, в которой этот командлет получает узлы DSC.

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

### -Status (состояние)
Задает состояние узлов DSC, которые получает этот командлет.
Допустимые значения: 

- SDMI 
- NotCompliant
- Ошибкой
- Типа 
- Получить
- Отвечать

```yaml
Type: DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases: 
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

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

### Microsoft. Azure. Commands. Automation. Model. DscNode

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Регистрация — AzureRmAutomationDscNode](./Register-AzureRmAutomationDscNode.md)

[Set-AzureRmAutomationDscNode](./Set-AzureRmAutomationDscNode.md)

[Отмена регистрации — AzureRmAutomationDscNode](./Unregister-AzureRmAutomationDscNode.md)


