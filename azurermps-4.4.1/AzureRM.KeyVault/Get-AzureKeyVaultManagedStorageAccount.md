---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: be4bf5b530fe1f40d7689bab935285b68b4a1b74
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104714761"
---
# Get-AzureKeyVaultManagedStorageAccount

## SYNOPSIS
Получает основные учетные записи хранилища Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## СИНТАКСИС

### ByVaultName (по умолчанию)
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAccountName
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Получает учетную запись хранилища Azure, управлия ключом, если задано имя учетной записи и управление ключами учетной записи происходит в указанном хранилище. Если имя учетной записи не указано, будут перечислены все учетные записи, ключами которых управляет указанный сейф.

## ПРИМЕРЫ

### Пример 1. Список всех ключевых учетных записей хранилища, управляемых хранилищем
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

Список всех учетных записей, ключами которых управляет хранилище Myvault.

### Пример 2. Получить учетную запись управляемого хранилища в key Vault
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

Подробные сведения о учетной записи хранилища mystorageaccount, если ключами управляет хранилище "myvault".

## PARAMETERS

### -AccountName
Имя учетной записи управляемого хранилища в key Vault. Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Имя сейфа.
Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Cmdlets key Vault Azure](/powershell/module/azurerm.keyvault/)
