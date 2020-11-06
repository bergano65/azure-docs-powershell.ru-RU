---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563332"
---
# Get-AzureRmADAppCredential

## КРАТКИй обзор
Извлекает список учетных данных, связанных с приложением.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ApplicationObjectIdParameterSet (по умолчанию)
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.

Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".

## ПАРАМЕТРЫ

### -ApplicationId
Идентификатор приложения, из которого извлекаются учетные данные.

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -ObjectId
Идентификатор объекта приложения, из которого извлекаются учетные данные.

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)

