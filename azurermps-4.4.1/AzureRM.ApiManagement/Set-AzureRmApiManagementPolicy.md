---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565713"
---
# Set-AzureRmApiManagementPolicy

## КРАТКИй обзор
Задает указанную политику области для управления API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Уровень клиента (по умолчанию)
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Уровень продукта
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Уровень API
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Уровень операций
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmApiManagementPolicy** задает указанную политику области для управления API.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка политики уровня клиента
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

Эта команда задает политику уровня клиента из файла с именем tenantpolicy.xml.

### Пример 2: Настройка политики для области продукта
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

Эта команда задает политику области продукта для управления API.

### Пример 3: Настройка политики области API
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

Эта команда задает политику области API для управления API.

### Пример 4: Настройка политики области действия
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

Эта команда задает политику области действия для управления API.

## ПАРАМЕТРЫ

### -ApiId
Указывает идентификатор существующего API.
Если указать этот параметр, командлет задает политику области API.

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Указывает экземпляр **PsApiManagementContext**.

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

### -Format
Задает формат политики.
Значением по умолчанию является "application/vnd. MS-Azure-apim. Policy + XML".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -С идентификатором
Указывает идентификатор существующей операции.
Если параметр задан с помощью ApiId, будет задана политика области действия.
Эти параметры являются обязательными.

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
PassThru

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Policy (политика)
Определяет документ политики в виде строки.
Этот параметр является обязательным, если не указан параметр- *PolicyFilePath* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyFilePath
Задает путь к файлу политики.
Этот параметр является обязательным, если параметр *политики* не указан.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductId
Указывает идентификатор существующего продукта.
Если указан этот параметр, командлет задает политику области продукта.

```yaml
Type: System.String
Parameter Sets: Product level
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

### логических

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Remove-AzureRmApiManagementPolicy](./Remove-AzureRmApiManagementPolicy.md)


