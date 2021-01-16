---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397655"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Удаляет существующий регион развертывания из экземпляра PsApiManagement.

## СИНТАКСИС

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **Remove-AzApiManagementRegion** удаляет экземпляр типа **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** из коллекции **AdditionalRegions** предоставленного экземпляра **типа Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.
Этот cmdlet не изменяют само развертывание, но обновляет экземпляр **PsApiManagement** в памяти.
Чтобы обновить развертывание управления API, передать измененный **psApiManagementInstance** в **Set-AzApiManagement.**

## ПРИМЕРЫ

### Пример 1. Удаление области из экземпляра PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Эта команда удаляет регион "Восток. США" из экземпляра **PsApiManagement.**

### Пример 2. Удаление области из экземпляра PsApiManagement с помощью ряда команд
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Эта первая команда получает экземпляр **PsApiManagement** из группы ресурсов Contoso с именем ContosoApi.
Затем конечная команда удаляет регион "Восток. США" из этого экземпляра, а затем обновляет развертывание.

## PARAMETERS

### -ApiManagement
Указывает экземпляр **PsApiManagement,** из который этот cmdlet удаляет дополнительный регион развертывания.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile

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

### -Location
Определяет расположение региона, который этот cmdlet удаляет.
Указывает расположение нового региона развертывания из поддерживаемого региона для службы управления Api.
Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


