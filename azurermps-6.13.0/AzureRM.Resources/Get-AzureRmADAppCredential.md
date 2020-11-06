---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564076"
---
# Get-AzureRmADAppCredential

## КРАТКИй обзор
Извлекает список учетных данных, связанных с приложением.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ApplicationObjectIdParameterSet (по умолчанию)
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.
Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.

## ИЛЛЮСТРИРУЮТ

### Пример 1. получение учетных данных приложения с помощью идентификатора объекта

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".

### Пример 2: получение учетных данных приложения с помощью трубопроводов

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

Возвращает приложение с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и преобразует его в командлет Get-AzureRmADAppCredential, чтобы получить список всех учетных данных для этого приложения.

## ПАРАМЕТРЫ

### -ApplicationId
Идентификатор приложения, из которого извлекаются учетные данные.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Объект приложения, из которого извлекаются учетные данные.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -DisplayName
Отображаемое имя приложения.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Идентификатор объекта приложения, из которого извлекаются учетные данные.

```yaml
Type: System.Guid
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

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication
Параметры: ApplicationObject (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)

