---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
ms.openlocfilehash: a07d9119d5e83c92d96ab22e98125459945f786b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562664"
---
# Update-AzureRmADUser

## КРАТКИй обзор
Обновление существующего пользователя Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### UPNOrObjectIdParameterSet (по умолчанию)
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UPNParameterSet
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Обновление существующего пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").
Дополнительные сведения: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser

## ИЛЛЮСТРИРУЮТ

### Пример 1. Изменение отображаемого имени пользователя с помощью идентификатора объекта

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

Обновляет отображаемое имя пользователя с идентификатором объекта "155a5c10-93a9-4941-a0df-96d83ab5ab24" и "MyNewDisplayName".

### Пример 2. Изменение отображаемого имени пользователя с помощью основного имени пользователя

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

Обновляет отображаемое имя пользователя с именем участника-пользователя " foo@domain.com " MyNewDisplayName ".

### Пример 3: изменение отображаемого имени пользователя с помощью трубопроводов

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

Возвращает пользователя с идентификатором объекта "155a5c10-93a9-4941-a0df-96d83ab5ab24" и каналами, которые должны использовать командлет Update-AzureRmADUser для обновления отображаемого имени пользователя на "MyNewDisplayName".

## ПАРАМЕТРЫ

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

### -DisplayName
Новое отображаемое имя пользователя.

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableAccount
значение true для включения учетной записи; в противном случае — значение false.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceChangePasswordNextLogin
Он должен быть указан, если пользователь должен сменить пароль при следующем успешном входе.
Только в том случае, если пароль обновлен, в противном случае он будет игнорироваться.

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

### -InputObject
Объект, представляющий пользователя, которого нужно обновить.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Идентификатор объекта пользователя, который необходимо обновить.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password (пароль)
Новый пароль пользователя.

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UPNOrObjectId
Имя участника-пользователя или код объекта пользователя, который нужно обновить.

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Имя субъекта-пользователя для обновляемого пользователя.

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

### System. GUID

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser
Параметры: InputObject (ByValue)

### System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]

### System. Security. SecureString

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
