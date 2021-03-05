---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991147"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Backs up a KeyVault-managed storage account.

## СИНТАКСИС

### ByStorageAccountName (по умолчанию)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Backup-AzKeyVaultManagedStorageAccount** можно создать резервную копию указанной учетной записи управляемого хранилища в хранилище ключа, скачав ее и храня в файле.
Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.
Вы можете восстановить запасную учетную запись хранения в любом хранилище ключей в подписке, из какой подписки она была, если хранилище находится в той же географической области Azure.
Этот cmdlet обычно используется по одной из причин: 
- Вы хотите сохранить автономный экземпляр учетной записи хранения на случай случайного удаления оригинала из хранилища.
 
- Вы создали учетную запись хранения с помощью хранилища ключей и хотите клонировать объект в другой регион Azure, чтобы использовать его из всех экземпляров распределенного приложения.
Используйте cmdlet **Backup-AzKeyVaultManagedStorageAccount** для получения учетной записи управляемого хранилища в зашифрованном формате, а затем используйте **cmdlet Restore-AzKeyVaultManagedStorageAccount** и укажите ключевое хранилище во втором регионе.

## ПРИМЕРЫ

### Пример 1. Архивная запись управляемого хранилища с автоматически созданным именем файла
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Эта команда извлекает учетную запись хранения MyMSAK из ключного хранилища MyKeyVault и сохраняет резервную копию этой учетной записи в файл, который автоматически именуется вам, и отображает имя файла.

### Пример 2. Архивная запись управляемого хранилища с указанным именем файла
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Эта команда извлекает учетную запись управляемого хранилища MyMSAK из ключного хранилища MyKeyVault и сохраняет ее резервную копию в файл Backup.blob.

### Пример 3. Архивная копия ранее восстановленной учетной записи управляемого хранилища на указанное имя файла, переописав файл назначения без запроса.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Эта команда создает резервную копию управляемой учетной записи хранения с именем $msak. Имя в хранилище с именем $msak. VaultName в файл Backup.blob, автоматически переописав файл, если он уже существует.

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

### -Force
Переописывать файл, если он существует

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
Пакет учетной записи хранения, который будет иметь запас, который будет совсююстрироваться с учетом результатов ирисовки звонка.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Секретное имя.
Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Выходной файл.
Выходной файл для хранения резервной копии учетной записи хранения.
Если он не задан, будет сгенерировано имя файла по умолчанию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Имя сейфа.
С его учетом именем и выбранной средой строится FQDN хранилища.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
