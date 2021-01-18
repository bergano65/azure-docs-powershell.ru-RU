---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518361"
---
# Backup-AzKeyVaultKey

## SYNOPSIS
Backs up a key in a key vault.

## СИНТАКСИС

### ByKeyName (по умолчанию)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Backup-AzKeyVaultKey** можно сделать резервную копию указанного ключа в хранилище ключей, скачав и храня его в файле.
Если есть несколько версий ключа, в резервную копию включаются все версии.
Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.
Вы можете восстановить подпапавную клавишу в любое хранилище ключей в подписке, из какой подписки она была.
Этот cmdlet обычно используется по одной из причин: 
- Вы хотите escrow a copy of your key, so that you have anfline copy in case you accidentally delete your key in your key vault.
 
- Вы создали ключ с помощью хранилища ключей и хотите клонировать его в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.
Используйте Restore-AzKeyVaultKey **Backup-AzKeyVaultKey** для получения ключа в зашифрованном формате, а затем используйте Restore-AzKeyVaultKey и укажите хранилище ключа во втором регионе.

## ПРИМЕРЫ

### Пример 1. Архивная архивная система ключа с автоматически созданным именем файла
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Эта команда извлекает ключ MyKey из хранилища ключей MyKeyVault и сохраняет его резервную копию в файл, который автоматически именуется вам, и отображает имя файла.

### Пример 2. Архивная архивная up a key to a specified file name
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Эта команда извлекает ключ MyKey из ключа MyKeyVault и сохраняет его резервную копию в файле Backup.blob.

### Пример 3. Архивная копия ранее извлеченного ключа на указанное имя файла, переописав файл назначения без запроса.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Эта команда создает резервную копию ключа с $key. Имя в хранилище с именем $key. VaultName в файл Backup.blob, автоматически переописав файл, если он уже существует.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -HsmName
Имя HSM. С его учетом именем и выбранной средой строится FQDN управляемой HSM- среды.

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Пакет ключей для повторного, проинтестрироваться на итоге ирисовки звонка.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Указывает имя ключа, который нужно сделать.

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Определяет выходной файл, в котором хранится BLOB-файл резервной копии.
Если этот параметр не задан, этот cmdlet создает имя файла.
Если указать имя существующего выходного файла, операция не будет завершена и выдаст сообщение об ошибке, указывающую, что файл резервной копии уже существует.

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
Указывает имя хранилища ключей, содержаного ключ для скайпа.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

