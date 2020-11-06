---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566995"
---
# Get-AzureKeyVaultKey

## КРАТКИй обзор
Получает ключи хранилища ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByVaultName (по умолчанию)
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectVaultName
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectKeyName
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKInputObjecteyVersions
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureKeyVaultKey** получает ключи Azure Key Vault.
Этот командлет получает определенный **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** или список всех объектов **KeyBundle** в хранилище ключей или по версии.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех ключей в хранилище ключей
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

Эта команда получает все ключи из хранилища ключей contoso.

### Пример 2: получение текущей версии ключа
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Эта команда получает текущую версию ключа с именем ITPfx в хранилище ключей contoso.

### Пример 3: получение всех версий ключа
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Эта команда возвращает все версии Key с именем ITPfx в разделе Key vaultnamed contoso.

### Пример 4: получение определенной версии ключа
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Эта команда возвращает определенную версию ключа с именем ITPfx в хранилище ключей, именуемом contoso.
После выполнения этой команды вы можете просматривать различные свойства ключа, перемещаясь по объекту $Key.

### Пример 5: получение всех ключей, которые были удалены, но не очищены для этого хранилища ключей.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Эта команда возвращает все разделы, которые были ранее удалены, но не очищены, в хранилище ключей contoso.

### Пример 6: получение ключа ITPfx, который был удален, но не очищен для этого хранилища ключей.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Эта команда возвращает клавишу ITPfx, которая была ранее удалена, но не очищена, в хранилище ключей, именуемом contoso.
Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного ключа.

## ПАРАМЕТРЫ

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

### -IncludeVersions
Указывает на то, что этот командлет получает все версии ключа.
Текущая версия ключа является первой в списке.
Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .

Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию ключа с указанным *именем*.

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект KeyVault.

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Указывает, нужно ли отображать ранее удаленные разделы в выходных данных.

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя набора ключей, который требуется получить.

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, из которого этот командлет получает ключи.
Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени, указанном этим параметром, и в выбранной среде.

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Указывает версию ключа.
Этот командлет создает полное доменное имя ключа на основе имени хранилища ключей, текущей выбранной среды, имени ключа и версии ключа.

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Подстрок

## НАПРЯЖЕНИЕ

### List<Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Undo-AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

