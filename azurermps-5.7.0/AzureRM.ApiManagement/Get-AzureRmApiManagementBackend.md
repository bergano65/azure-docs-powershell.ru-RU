---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 0074ed7ec0d3aa88f813d138be71083195e6b10a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559384"
---
# Get-AzureRmApiManagementBackend

## КРАТКИй обзор
Получение подробных сведений о внутреннем сервере.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### GetAllBackends (по умолчанию)
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByBackendId
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Получение подробных сведений о внутреннем сервере.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех незавершенных элементов
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

Получает список всех незавершенных элементов, настроенных в службе управления API.

### Пример 2: получение серверной части, указанной идентификатором 123
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

Получение сведений об указанной серверной части, идентифицированной с помощью идентификатора "123"

## ПАРАМЕТРЫ

### -BackendId
Идентификатор внутреннего сервера.
Если задано значение, это попытается найти сервер по идентификатору.
Этот параметр является необязательным.

```yaml
Type: String
Parameter Sets: GetByBackendId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Экземпляр PsApiManagementContext.
Этот параметр является обязательным.

```yaml
Type: PsApiManagementContext
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend
Сведения о серверной части, настроенной в службе управления API.

### IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend>
Список внутренних баз данных, настроенных в службе управления API.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmApiManagementBackend](./New-AzureRmApiManagementBackend.md)

[New-AzureRmApiManagementBackendCredential](./New-AzureRmApiManagementBackendCredential.md)

[New-AzureRmApiManagementBackendProxy](./New-AzureRmApiManagementBackendProxy.md)

[Set-AzureRmApiManagementBackend](./Set-AzureRmApiManagementBackend.md)

[Remove-AzureRmApiManagementBackend](./Remove-AzureRmApiManagementBackend.md)
