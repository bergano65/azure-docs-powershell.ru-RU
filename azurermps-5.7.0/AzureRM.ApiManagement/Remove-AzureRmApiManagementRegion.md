---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570323"
---
# Remove-AzureRmApiManagementRegion

## КРАТКИй обзор
Удаляет существующий регион развертывания из экземпляра PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmApiManagementRegion** удаляет экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** из коллекции **AdditionalRegions** предоставленных экземпляров типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Этот командлет не изменяет само развертывание, но обновляет экземпляр **PsApiManagement** в памяти.
Чтобы обновить развертывание управления API, передайте модифицированный **PsApiManagementInstance** на **Update-AzureRmApiManagement**.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление региона из экземпляра PsApiManagement
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Эта команда удаляет из экземпляра **PsApiManagement** регион с именем "Восток США".

### Пример 2: удаление региона из экземпляра PsApiManagement с помощью ряда команд
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

Эта первая команда получает экземпляр **PsApiManagement** из группы ресурсов contoso с именем ContosoApi.
Последняя команда затем удаляет из этого экземпляра регион с именем "Восток США" и обновляет развертывание.

## ПАРАМЕТРЫ

### -ApiManagement
Указывает экземпляр **PsApiManagement** , из которого этот командлет удаляет дополнительный регион развертывания.

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.
 
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

### -Location
Указывает расположение области, которую удаляет этот командлет.

Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.
Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PsApiManagement
Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


