---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912740"
---
# Backup-AzKeyVaultManagedStorageAccount

## КРАТКИй обзор
Создание резервной копии управляемой учетной записи хранения KeyVault.

## Максимальное

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

## NОПИСАНИЕ
Командлет **BACKUP-AzKeyVaultManagedStorageAccount** используется для резервного копирования указанной управляемой учетной записи хранения в хранилище ключей, загружая ее и сохраняя в файле.
Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.
Вы можете восстановить резервную учетную запись хранения в любом хранилище ключей в подписке, в которой она была создана из резервной копии, если она находится в том же географическом элементе Azure.
Ниже приведены основные причины использования этого командлета. 
- Вы хотите сохранить автономную копию учетной записи хранения на случай, если вы случайно удалили оригинал из хранилища.
 
- Вы создали управляемую учетную запись хранения с помощью ключа Vault и теперь хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.
С помощью командлета **BACKUP-AzKeyVaultManagedStorageAccount** можно получить управляемую учетную запись хранения в зашифрованном формате, а затем использовать командлет **RESTORE-AzKeyVaultManagedStorageAccount** и указав ключевое хранилище во втором регионе.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание резервной копии управляемой учетной записи хранения с автоматически созданным именем файла
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Эта команда извлекает управляемую учетную запись хранения с именем MyMSAK из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этой управляемой учетной записи хранения в файле с автоматическим именем и выводит имя файла.

### Пример 2: создание резервной копии управляемой учетной записи хранения в указанном имени файла
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Эта команда извлекает управляемую учетную запись хранения с именем MyMSAK из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этой управляемой учетной записи хранения в файле с именем Backup. BLOB.

### Пример 3: создание резервной копии ранее полученной управляемой учетной записи хранения в указанном имени файла с перезазаписьм конечного файла без запроса.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Эта команда создает резервную копию управляемой учетной записи хранения с именем $msak. Имя в хранилище с именем $msak. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.

## ПАРАМЕТРЫ

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
Перезаписать заданный файл, если он существует

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
Набор учетных записей хранилища для резервного копирования, конвейера, из результатов запроса на получение.

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

### -Name (имя)
Имя секрета.
Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.

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

### -Выходной_файл
Выходной файл.
Выходной файл для хранения резервной копии учетной записи хранения.
Если не указано, будет создано имя файла по умолчанию.

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
Имя хранилища.
Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
