---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567193"
---
# Get-AzureRmApiManagementLogger

## КРАТКИй обзор
Возвращает объекты средства ведения журнала управления API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Получение всех средств ведения журнала (по умолчанию)
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Получить с помощью идентификатора регистратора
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmApiManagementLogger** получает **средство ведения журнала** управления API Azure или все средства ведения журнала.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех средств ведения журнала
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

Эта команда получает все средства ведения журнала для указанного контекста.

### Пример 2: получение определенного средства ведения журнала
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

Эта команда удаляет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.

## ПАРАМЕТРЫ

### -Context
Указывает объект **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoggerId
Указывает идентификатор определенного регистратора, который требуется получить.

```yaml
Type: System.String
Parameter Sets: Get by logger ID
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger>

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmApiManagementLogger](./New-AzureRmApiManagementLogger.md)

[Remove-AzureRmApiManagementLogger](./Remove-AzureRmApiManagementLogger.md)

[Set-AzureRmApiManagementLogger](./Set-AzureRmApiManagementLogger.md)


