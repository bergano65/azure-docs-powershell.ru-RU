---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911171"
---
# Get-AzKeyVaultSecret

## КРАТКИй обзор
Возвращает секреты в хранилище ключей.

## Максимальное

### ByVaultName (по умолчанию)
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzKeyVaultSecret** получает секреты в хранилище ключей.
Этот командлет получает определенный секрет или все секреты в хранилище ключей.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех текущих версий всех секретных данных в хранилище ключей
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

Эта команда возвращает текущие версии всех секретных данных в хранилище ключей, именуемом contoso.

### Пример 2: получение всех версий определенного секрета
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Эта команда получает все версии секрета с именем ITSecret в хранилище ключей, именуемом contoso.

### Пример 3: получение текущей версии определенного секрета
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Эта команда получает текущую версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.

### Пример 4: получение определенной версии определенного секрета
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Эта команда возвращает определенную версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.

### Пример 5: получение простого текстового значения текущей версии определенного секрета
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Эти команды получают текущую версию секрета с именем ITSecret и выводят на экран значение в формате обычного текста этого секрета.

### Пример 6: получение всех секретов, которые были удалены, но не очищены для этого хранилища ключей.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Эта команда получает все секретные данные, которые были ранее удалены, но не очищены, в хранилище ключей, именуемом contoso.

### Пример 7: возвращает секретный ITSecret, который был удален, но не очищен для этого хранилища ключей.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Эта команда получает секретный ITSecret, который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.
Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного секрета.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeVersions
Указывает на то, что этот командлет получает все версии секрета.
Текущая версия секрета является первой в списке.
Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .

Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию секрета с указанным *именем*.

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Указывает, нужно ли отображать ранее удаленные секреты в выходных данных.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя секрета для получения.

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, к которому относится секрет.
Этот командлет создает полное доменное имя (FQDN) хранилища ключей, основываясь на имени, которое указывает этот параметр, и текущую среду.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Указывает секретную версию.
Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Подстрок

## НАПРЯЖЕНИЕ

### List<Microsoft. Azure. Commands. KeyVault. Models. SecretIdentityItem>, Microsoft. Azure.,. KeyVault. Models. Secret, List<Microsoft. Azure. Commands. KeyVault>. Models. DeletedSecretIdentityItem

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Undo-AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

