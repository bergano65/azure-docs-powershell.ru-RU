---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563763"
---
# Publish-AzureRmApiManagementTenantGitConfiguration

## КРАТКИй обзор
Публикует изменения из ветви Git в базу данных конфигурации.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Publish-AzureRmApiManagementTenantGitConfiguration** публикует изменения из ветви Git в базу данных конфигурации.
Вы также можете проверить изменения в ветви Git без публикации.

## ИЛЛЮСТРИРУЮТ

### Пример 1: развертывание изменений Git
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

Эта команда публикует изменения из указанной ветви в базу данных конфигурации.

### Пример 2: Проверка изменений Git
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

Эта команда проверяет изменения в ветви Git в соответствии с базой данных конфигурации.
Изменения не публикуются.

## ПАРАМЕТРЫ

### -Branch
Указывает имя ветви Git, из которой этот командлет развертывает конфигурацию в базе данных конфигурации.

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

### -Context
Указывает объект **PsApiManagementContext** .

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

### -Force
Указывает, что этот командлет удаляет подписку на продукты, удаленные в этом обновлении.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Указывает на то, что этот командлет возвращает объект **PsApiManagementOperationResult** .

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidateOnly
Указывает, что этот командлет проверяет изменения в указанной ветви Git.
Она не публикуется в базе данных конфигурации.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Сохранить — AzureRmApiManagementTenantGitConfiguration](./Save-AzureRmApiManagementTenantGitConfiguration.md)


