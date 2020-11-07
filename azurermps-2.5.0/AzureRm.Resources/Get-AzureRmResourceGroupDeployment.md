---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913423"
---
# Get-AzureRmResourceGroupDeployment

## КРАТКИй обзор
Возвращает развертывания в группе ресурсов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### GetByResourceGroupDeploymentName (по умолчанию)
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmResourceGroupDeployment** получает развертывание в группе ресурсов Azure.
Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.
По умолчанию **Get-AzureRmResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.
Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.
Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.
Развертывание — это операция, которая делает ресурсы в группе ресурсов доступной для использования.
Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.
Вы можете использовать этот командлет для отслеживания.
Для отладки используйте этот командлет с командлетом Get-AzureRmLog.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех развертываний для группы ресурсов
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.
На выходе показано развертывание для блога WordPress, в котором был использован шаблон коллекции.

### Пример 2: получение развертывания по имени
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.
Вы можете присвоить имя развертыванию при создании с помощью командлетов **New-AzureRmResourceGroup** или **New-AzureRmResourceGroupDeployment** .
Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.

### Пример 3: получение развертываний всех групп ресурсов
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Эта команда получает все группы ресурсов в подписке с помощью командлета Get-AzureRmResourceGroup.
Команда передает группы ресурсов в текущий командлет с помощью оператора конвейера.
Текущий командлет получает все развертывания всех групп ресурсов в подписке и передает результаты в командлет Format-Table, чтобы отобразить значения свойств **ResourceGroupName** , **DeploymentName** и **ProvisioningState** .

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
Указывает идентификатор развертывания группы ресурсов, который требуется получить.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя развертывания, которое требуется получить.
Подстановочные знаки не разрешены.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
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
Указывает имя группы ресурсов.
Командлет получает развертывание для группы ресурсов, которую указывает этот параметр.
Подстановочные знаки не разрешены.
Этот параметр является обязательным, и вы можете указать только одну группу ресурсов в каждой команде.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Остановить-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


