---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560168"
---
# Backup-AzureKeyVaultCertificate

## КРАТКИй обзор
Создание резервной копии сертификата в хранилище ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByCertificateName (по умолчанию)
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **BACKUP-AzureKeyVaultCertificate** производит резервное копирование указанного сертификата в хранилище ключей, загружая его и сохраняя в файле.
Если у сертификата есть несколько версий, все их версии будут включены в резервную копию.
Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.
Вы можете восстановить резервную копию сертификата в любом хранилище ключей в подписке, из которой она была создана, пока она находится в том же географическом расположении Azure.
Ниже приведены основные причины использования этого командлета. 
- Вы хотите сохранить автономную копию сертификата на случай, если вы случайно удалили оригинал из хранилища.
 
- Вы создали сертификат с помощью ключа Vault и теперь хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.
С помощью командлета **BACKUP-AzureKeyVaultCertificate** можно получить сертификат в зашифрованном формате, а затем использовать командлет **RESTORE-AzureKeyVaultCertificate** и указав для него хранилище ключей во втором регионе.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание резервной копии сертификата с автоматически сгенерированным именем файла
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Эта команда извлекает сертификат с именем MyCert из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого сертификата в файл с автоматическим именем и выводит имя файла.

### Пример 2: создание резервной копии сертификата для указанного имени файла
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Эта команда извлекает сертификат с именем MyCert из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого сертификата в файле с именем Backup. BLOB.

### Пример 3: создание резервной копии ранее полученного сертификата по указанному имени файла с перезазаписьм конечного файла без запроса.
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Эта команда создает резервную копию сертификата с именем $cert. Имя в хранилище с именем $cert. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.

## ПАРАМЕТРЫ

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
Секрет, для которого необходимо создать резервную копию, конвейер из результатов запроса на получение.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

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
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Выходной_файл
Выходной файл.
Выходной файл, в котором будет храниться резервная копия сертификата.
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
Parameter Sets: ByCertificateName
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem
Параметры: InputObject (ByValue)

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
