---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: 1a2445509aca49c28320ad1fc1685daa0127fa50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561772"
---
# Backup-AzureKeyVaultSecret

## КРАТКИй обзор
Резервное копирование секрета в хранилище ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### BySecretName (по умолчанию)
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **BACKUP-AzureKeyVaultSecret** производит резервное копирование указанного секрета в качестве ключа, загружая его и сохраняя в файле.
Если существует несколько версий секрета, в резервную копию включаются все версии.
Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.
Вы можете восстановить резервные копии в любом хранилище ключей в подписке, из которой она была создана.

Ниже приведены основные причины использования этого командлета.

- Вы хотите пополнить свою копию секрета, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили свой секрет в своем вашем хранилище ключей.
- Вы добавили секрет в хранилище ключей и теперь хотите клонировать секрет в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения. С помощью командлета Backup-AzureKeyVaultSecret можно получить секретный код в зашифрованном формате, а затем использовать командлет Restore-AzureKeyVaultSecret и указать в качестве него ключевое хранилище во втором регионе. (Обратите внимание, что регионы должны принадлежать одному и тому же географическому элементу.)

## ИЛЛЮСТРИРУЮТ

### Пример 1: резервное копирование секрета с автоматически сгенерированным именем файла
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

Эта команда извлекает секретный файл с именем MySecret из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого секрета в файле, который будет автоматически называться, и выводит имя файла.

### Пример 2: создание резервной копии секретного файла с заданным именем и перезапись существующего файла без запроса
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

Эта команда извлекает секрет с именем MySecret из ключа vaultnamed MyKeyVault и сохраняет резервную копию этого секрета в файле с именем Backup. BLOB.

### Пример 3: создание резервной копии ранее извлеченного секретного файла с указанным именем
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

Эта команда использует имя и имя хранилища объекта $secret, чтобы получить секрет и сохранит его резервную копию в файле с именем Backup. BLOB.

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
Запрашивает подтверждение перед перезаписью выходного файла, если он существует.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Секрет, для которого необходимо создать резервную копию, конвейер из результатов запроса на получение.

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Задает имя секрета для резервного копирования.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

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
Указывает имя хранилища ключей, содержащего секрет для резервного копирования.

```yaml
Type: String
Parameter Sets: BySecretName
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
Default value: False
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
Default value: False
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

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Restore-AzureKeyVaultSecret](./Restore-AzureKeyVaultSecret.md)

