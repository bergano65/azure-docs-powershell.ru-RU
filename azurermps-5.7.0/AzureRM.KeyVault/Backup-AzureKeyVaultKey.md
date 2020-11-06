---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2eecb6d4bb069b1578b3080c04de4c9df1e42f09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561771"
---
# Backup-AzureKeyVaultKey

## КРАТКИй обзор
Резервное копирование ключа в хранилище ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByKeyName (по умолчанию)
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **BACKUP-AzureKeyVaultKey** используется для резервного копирования указанного ключа в хранилище ключей, загружая его и сохраняя в файле.
Если вы используете несколько версий ключа, в резервную копию включаются все версии.
Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.
Вы можете восстановить резервную копию ключа в любом хранилище ключей в подписке, из которой она была создана.

Ниже приведены основные причины использования этого командлета. 

- Вы хотите пополнить свою копию ключа, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили ключ в своем вашем хранилище ключей.
 
- Вы создали ключ с помощью ключевого хранилища, и теперь хотите клонировать ключ в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.
С помощью командлета **BACKUP-AzureKeyVaultKey** можно получить ключ в зашифрованном формате, а затем воспользоваться командлетом Restore-AzureKeyVaultKey и указать в качестве него ключевое хранилище во втором регионе.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание резервной копии ключа с автоматически сгенерированным именем файла
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

Эта команда извлекает ключ с именем MyKey из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого ключа в файле с автоматическим именем и выводит имя файла.

### Пример 2: создание резервной копии ключа для указанного имени файла
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

Эта команда извлекает ключ с именем MyKey из ключа vaultnamed MyKeyVault и сохраняет резервную копию этого ключа в файл с именем Backup. BLOB.

### Пример 3: создание резервной копии ранее полученного ключа в указанном файле, перезапись файла назначения без запроса.
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

Эта команда создает резервную копию ключа с именем $key. Имя в хранилище с именем $key. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.

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

### -Force
Перезаписать заданный файл, если он существует

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Набор ключей для резервного копирования, конвейера из выходных данных вызова.

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Задает имя ключа для резервного копирования.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Выходной_файл
Указывает выходной файл, в котором хранится резервная копия (BLOB-объект).
Если этот параметр не указан, этот командлет создаст имя файла.
Если вы задаете имя существующего выходного файла, операция не завершится и вернет сообщение об ошибке, в котором файл резервной копии уже существует.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, содержащего ключ для резервного копирования.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Подстрок
Командлет возвращает путь к выходному файлу, содержащему резервную копию ключа.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Restore-AzureKeyVaultKey](./Restore-AzureKeyVaultKey.md)

