---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://go.microsoft.com/fwlink/?LinkId=690298
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f6fca9ec6b5f5696cbaa1fb82942e5aa6dfadf80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559787"
---
# Get-AzureKeyVaultSecret

## КРАТКИй обзор
Возвращает секреты в хранилище ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByVaultName (по умолчанию)
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureKeyVaultSecret** получает секреты в хранилище ключей.
Этот командлет получает определенный секрет или все секреты в хранилище ключей.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех текущих версий всех секретных данных в хранилище ключей
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

Эта команда возвращает текущие версии всех секретных данных в хранилище ключей, именуемом contoso.

### Пример 2: получение всех версий определенного секрета
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Эта команда получает все версии секрета с именем ITSecret в хранилище ключей, именуемом contoso.

### Пример 3: получение текущей версии определенного секрета
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Эта команда получает текущую версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.

### Пример 4: получение определенной версии определенного секрета
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Эта команда возвращает определенную версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.

### Пример 5: получение простого текстового значения текущей версии определенного секрета
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Эти команды получают текущую версию секрета с именем ITSecret и выводят на экран значение в формате обычного текста этого секрета.

### Пример 6: получение всех секретов, которые были удалены, но не очищены для этого хранилища ключей.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Эта команда получает все секретные данные, которые были ранее удалены, но не очищены, в хранилище ключей, именуемом contoso.

### Пример 7: возвращает секретный ITSecret, который был удален, но не очищен для этого хранилища ключей.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Эта команда получает секретный ITSecret, который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.
Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного секрета.

## ПАРАМЕТРЫ

### -IncludeVersions
Указывает на то, что этот командлет получает все версии секрета.
Текущая версия секрета является первой в списке.
Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .

Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию секрета с указанным *именем*.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, к которому относится секрет.
Этот командлет создает полное доменное имя (FQDN) хранилища ключей, основываясь на имени, которое указывает этот параметр, и текущую среду.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Указывает секретную версию.
Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 3
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Подстрок

## НАПРЯЖЕНИЕ

### List<Microsoft. Azure. Commands. KeyVault. Models. SecretIdentityItem>, Microsoft. Azure.,. KeyVault. Models. Secret, List<Microsoft. Azure. Commands. KeyVault>. Models. DeletedSecretIdentityItem

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Undo-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

