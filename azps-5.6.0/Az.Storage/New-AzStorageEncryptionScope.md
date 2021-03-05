---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002456"
---
# New-AzStorageEncryptionScope

## SYNOPSIS
Создает область шифрования для учетной записи хранения.

## СИНТАКСИС

### AccountName (по умолчанию)
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountNameKeyVault
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AccountObjectKeyVault
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для учетной записи хранения создается область шифрования **New-AzStorageEncryptionScope.**

## ПРИМЕРЫ

### Пример 1. Создание области шифрования с помощью шифрования хранилища
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

Эта команда создает область шифрования с помощью шифрования хранилища.

### Пример 2. Создание области шифрования с помощью шифрования Keyvault и RequireInfrastructureEncryption
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

Эта команда создает область шифрования с шифрованием Keyvault и RequireInfrastructureEncryption.
Удостоверение учетной записи хранения должен иметь разрешения на доступ к клавише keyvault, переносы, а также разрешение на перенос.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionScopeName
Имя службы шифрования хранилищ Azure

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyUri
Uri ключа

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyvaultEncryption
Создание области шифрования с помощью keySource в качестве Microsoft.Keyvault

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireInfrastructureEncryption
В области шифрования будет применяться дополнительный уровень шифрования с управляемыми платформой ключами для неавторяых данных.

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

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
Объект учетной записи хранения

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Имя учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageEncryption
Создайте область шифрования с помощью keySource в качестве Microsoft.Storage.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## OUTPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
