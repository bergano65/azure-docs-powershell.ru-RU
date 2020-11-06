---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561508"
---
# Install-AzureRmServerManagementGatewayProfile

## КРАТКИй обзор
Установка профиля шлюза управления сервером.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Install-AzureRmServerManagementGatewayProfile** устанавливает профиль шлюза службы управления сервером Azure Server в нужное расположение.
Файл, который устанавливает этот командлет, называется profile.js.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

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

### -InputFile
Указывает имя локального файла, который содержит профиль шлюза для установки.

Файл, который устанавливает этот командлет, должен быть ранее сохранен с помощью командлета Save-AzureRmServerManagementGatewayProfile.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### FileInfo
Параметр "InputFile" принимает значение типа FileInfo из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Сброс — AzureRmServerManagementGatewayProfile](./Reset-AzureRmServerManagementGatewayProfile.md)

[Сохранить — AzureRmServerManagementGatewayProfile](./Save-AzureRmServerManagementGatewayProfile.md)


