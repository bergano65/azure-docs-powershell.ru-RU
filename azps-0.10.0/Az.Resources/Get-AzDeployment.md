---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: d47660d5867c1d7f9fad04884ba66c9e2c996900
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910956"
---
# Get-AzDeployment

## КРАТКИй обзор
Получить развертывание

## Максимальное

### GetByDeploymentName (по умолчанию)
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzDeployment** получает развертывание в текущей области подписки.
Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.
По умолчанию **Get-AzDeployment** получает все развертывания в текущей области подписки.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех развертываний в области подписки
```
PS C:\>Get-AzDeployment
```

Эта команда получает все развертывания в текущей области подписки.

### Пример 2: получение развертывания по имени
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

Эта команда получает развертывание DeployRoles01 в текущей области подписки.
Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzDeployment** .
Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.

## ПАРАМЕТРЫ

### -ApiVersion
Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.
Если не указано, версия API автоматически определяется как самая свежая доступная.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Полный идентификатор ресурса для развертывания.
Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя развертывания.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
