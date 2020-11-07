---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: ca40a9b74dd92b7bcdecdde87e4763f044b3272f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727967"
---
# Remove-AzApiManagementRegion

## КРАТКИй обзор
Удаляет существующий регион развертывания из экземпляра PsApiManagement.

## Максимальное

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzApiManagementRegion** удаляет экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** из коллекции **AdditionalRegions** предоставленных экземпляров типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Этот командлет не изменяет само развертывание, но обновляет экземпляр **PsApiManagement** в памяти.
Чтобы обновить развертывание управления API, передайте модифицированный **PsApiManagementInstance** в **Set-AzApiManagement**.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление региона из экземпляра PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Эта команда удаляет из экземпляра **PsApiManagement** регион с именем "Восток США".

### Пример 2: удаление региона из экземпляра PsApiManagement с помощью ряда команд
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Эта первая команда получает экземпляр **PsApiManagement** из группы ресурсов contoso с именем ContosoApi.
Последняя команда затем удаляет из этого экземпляра регион с именем "Восток США" и обновляет развертывание.

## ПАРАМЕТРЫ

### -ApiManagement
Указывает экземпляр **PsApiManagement** , из которого этот командлет удаляет дополнительный регион развертывания.

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
Указывает расположение области, которую удаляет этот командлет.
Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.
Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


