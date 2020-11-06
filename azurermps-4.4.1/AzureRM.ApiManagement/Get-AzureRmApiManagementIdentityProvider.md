---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565760"
---
# Get-AzureRmApiManagementIdentityProvider

## КРАТКИй обзор
Получение сведений о конфигурации поставщика удостоверений.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### AllIdentityProviders (по умолчанию)
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdentityProviderByType
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Получение сведений о конфигурации поставщика удостоверений.

## ИЛЛЮСТРИРУЮТ

### --------------------------Пример 1--------------------------
@ {абзац = PS C: \\ \> }







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

Получение всех конфигураций поставщика удостоверений в службе.

### --------------------------Пример 2--------------------------
@ {абзац = PS C: \\ \> }







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

Возвращает конфигурацию поставщика удостоверений Azure Active Directory.

## ПАРАМЕТРЫ

### -Context
Экземпляр PsApiManagementContext.
Этот параметр является обязательным.

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

### -Type (тип)
Идентификатор поставщика удостоверений.
Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.
Этот параметр является необязательным.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

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

### IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider>

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

