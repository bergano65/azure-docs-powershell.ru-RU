---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 6c076258acd19714f30976fd353d7cbbacdf1d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560687"
---
# Remove-AzureRmADAppCredential

## КРАТКИй обзор
Удаление учетных данных из приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ApplicationObjectIdWithKeyIdParameterSet (по умолчанию)
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdWithKeyIdParameterSet
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationDisplayNameParameterSet
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyIdParameterSet
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Remove-AzureRmADAppCredential можно использовать для удаления ключа учетных данных из приложения в случае раскрытия или в рамках истечения срока действия смены ключа учетных данных.
Приложение определяется путем указания идентификатора объекта или AppId.
Удаляемые учетные данные определяются с помощью ее кода ключа.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление определенных учетных данных из приложения

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Удаляет учетные данные с ИД ключа "9044423a-60a3-45AC-9ab1-09534157ebb" из приложения с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82".

### Пример 2. Удаление всех учетных данных из приложения

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

Удаляет все учетные данные из приложения с идентификатором приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".

### Пример 3. Удаление всех учетных данных с помощью трубопроводов

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

Возвращает приложение с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" и каналами, которые будут использовать командлет Remove-AzureRmADAppCredential, и удаляет все учетные данные из этого приложения.

## ПАРАМЕТРЫ

### -ApplicationId
Идентификатор приложения, из которого нужно удалить учетные данные.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Объект приложения, из которого нужно удалить учетные данные.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
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
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Переключиться в режим удаления учетных данных без подтверждения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Указывает ключ учетных данных, который нужно удалить.
Коды клавиш для приложения можно получить с помощью командлета Get-AzureRmADAppCredential.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Идентификатор объекта приложения, из которого нужно удалить учетные данные.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Если указать это, будет возвращено значение истина, если команда была выполнена успешно.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[New-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)
