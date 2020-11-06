---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558588"
---
# Update-AzureRmApiManagementRegion

## КРАТКИй обзор
Обновляет существующий регион развертывания в экземпляре PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Update-AzureRmApiManagementRegion** обновляет существующий экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** в коллекции объектов **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Этот командлет не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.
Чтобы обновить развертывание управления API, используйте модифицированный **PsApiManagementInstance** в командлете Update-AzureRmApiManagementDeployment.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -ApiManagement
Указывает экземпляр **PsApiManagement** , который будет обновлять существующий регион развертывания в.

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

### -Capacity
Указывает новое значение емкости SKU для региона развертывания.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Location
Указывает расположение области развертывания для обновления.
Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.
Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object

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

### -SKU
Задает значение нового уровня для области развертывания.
Допустимые значения:
- Программист
- Стандартная
- Версию

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Указывает конфигурацию виртуальной сети для региона развертывания.
Передача $null приведет к удалению конфигурации виртуальной сети для региона.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement
Параметры: ApiManagement (ByValue)

### System. String

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku

### System. Int32

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)
