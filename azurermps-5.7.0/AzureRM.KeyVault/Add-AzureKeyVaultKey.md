---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 153cd3099b750732e281992e98cdafb173a71276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566625"
---
# Add-AzureKeyVaultKey

## КРАТКИй обзор
Создание ключа в хранилище ключей или импорт ключа в хранилище ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### InteractiveCreate (по умолчанию)
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureKeyVaultKey** создает ключ в хранилище ключей в хранилище ключей Azure или импортирует ключ в хранилище ключей.
Используйте этот командлет для добавления клавиш одним из следующих способов:

- Создание ключа в аппаратном модуле безопасности (HSM) в службе хранилища ключей.
- Создание ключа в программном обеспечении в службе хранилища ключей.
- Импортируйте ключ из собственного модуля безопасности оборудования (HSM) в HSMs в службе хранилища ключей.
- Импорт ключа из PFX-файла на компьютере.
- Импорт ключа из PFX-файла на компьютере в модули безопасности оборудования (HSMs) в службе хранилища ключей.

Для любой из этих операций можно задать ключевые атрибуты или оставить параметры по умолчанию.

Если вы создаете или импортируете ключ с тем же именем, что и у существующего ключа в вашем хранилище ключей, первоначальный ключ обновляется с учетом значений, которые вы указали для нового ключа. Вы можете получить доступ к предыдущим значениям, используя универсальный код ресурса (URI) для указанной версии ключа. Чтобы узнать о ключевых версиях и структуре URI, ознакомьтесь со статьей о ключах [andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) в документации по API-интерфейсу для хранилища ключей.

Примечание. чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK. Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).

Рекомендуется создать резервную копию ключа после его создания или обновления с помощью командлета Backup-AzureKeyVaultKey. Функция отмены удаления отсутствует, поэтому если вы случайно удалили ключ или удалите его, а затем передумали, ключ не подлежит восстановлению, только если у вас есть резервная копия, которую вы можете восстановить.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание ключа
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

Эта команда создает ключ с защитой программного обеспечения с именем ITSoftware в хранилище ключей, именуемом contoso.

### Пример 2: создание ключа, защищенного с помощью HSM
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

Эта команда создает ключ, защищенный HSM, в хранилище ключей, именуемом contoso.

### Пример 3: создание ключа с использованием значений, не заданных по умолчанию
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

Первая команда сохраняет значения для расшифровки и проверки в переменной $KeyOperations.

Вторая команда создает объект **DateTime** , определенный в формате UTC, с помощью командлета **Get-Date** .
Этот объект указывает на время в будущем на два года. Команда сохраняет эту дату в переменной $Expires. Для получения дополнительных сведений введите `Get-Help Get-Date` .

Третья команда создает объект **DateTime** с помощью командлета **Get-Date** . Этот объект указывает текущее время в формате UTC. Команда сохраняет эту дату в переменной $NotBefore.

Последняя команда создает ключ с именем ITHsmNonDefault, который является ключом, защищенным с помощью HSM. Команда задает значения разрешенных операций с ключами, сохраненными $KeyOperations. В команде указаны значения времени для параметров *Expires* и *NotBefore* , созданных в предыдущих командах, а также теги для высокого уровня важности и. Новый ключ отключен. Это можно сделать с помощью командлета **Set-AzureKeyVaultKey** .

### Пример 4: импорт ключа, защищенного с помощью HSM
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

Эта команда импортирует ключ с именем ITByok из расположения, указанного параметром *KeyFilePath* . Импортированный ключ является ключом, защищенным с помощью HSM.

Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.
Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).

### Пример 5: импорт ключа, защищенного с помощью программного обеспечения
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password. Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .

Вторая команда создает пароль программного обеспечения в хранилище ключей contoso. Команда задает расположение ключа и пароль, хранящийся в $Password.

### Пример 6: импорт ключа и назначение атрибутов
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.

Вторая команда создает объект **DateTime** с помощью командлета **Get-Date** , а затем сохраняет этот объект в переменной $Expires.

Третья команда создает переменную $tags, чтобы установить теги для высокого уровня важности и.

Последняя команда импортирует ключ в качестве ключа HSM из указанного места. Команда задает срок действия, хранящийся в $Expires и пароль, которые хранятся в $Password, и применяет теги, хранящиеся в $tags.

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

### -Destination
Указывает, следует ли добавить ключ в качестве ключа с защитой программного обеспечения или ключа, защищенного с помощью HSM, в службе хранилища ключей.
Допустимые значения: HSM и программное обеспечение.

Примечание. чтобы использовать HSM в качестве места назначения, необходимо иметь ключевое хранилище, которое поддерживает HSMs. Дополнительные сведения о уровнях обслуживания и возможностях Azure Key Vault можно найти на [веб-сайте ценообразования для Azure Key Vault](https://go.microsoft.com/fwlink/?linkid=512521).

Этот параметр является обязательным при создании нового ключа. При импорте ключа с помощью параметра *KeyFilePath* этот параметр является необязательным:

- Если этот параметр не указан, а этот командлет импортирует ключ с расширением byok, он импортирует этот ключ в качестве ключа, защищенного с помощью HSM-файлов. Командлет не может импортировать эту клавишу в качестве ключа, защищенного с помощью программного обеспечения.

- Если этот параметр не указан, а этот командлет импортирует ключ с расширением имени PFX-файла, он импортирует ключ как ключ, защищенный программным обеспечением.

```yaml
Type: String
Parameter Sets: InteractiveCreate, InputObjectCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отключение
Указывает на то, что для добавляемого ключа задано начальное состояние "отключено". Любая попытка использования ключа завершится сбоем. Используйте этот параметр, если нужно предварительно загрузить ключи, которые нужно включить в дальнейшем.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Истекает
Задает время истечения срока действия в виде объекта **DateTime** для ключа, который добавляется этим командлетом. Этот параметр использует координированное координированное время (UTC). Чтобы получить объект **DateTime** , используйте командлет **Get-Date** . Для получения дополнительных сведений введите `Get-Help Get-Date` . Если этот параметр не указан, срок действия ключа не истекает.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Объект хранилища.

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Указывает пароль для импортированного файла как объект **SecureString** . Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** . Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` . Вы должны указать этот пароль, чтобы импортировать файл с расширением имени PFX-файла.

```yaml
Type: SecureString
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Указывает путь к локальному файлу, содержащему ключевой материал, который этот командлет импортирует.
Допустимые расширения имен файлов: byok и PFX.

- Если файл является файлом byok, ключ автоматически защищается HSMs после импорта, и вы не сможете переопределить этот параметр по умолчанию.

- Если файл является PFX-файлом, ключ автоматически защищается программным путем после импорта. Чтобы переопределить это значение по умолчанию, установите для параметра *Destination* значение HSM, чтобы ключ был защищен с помощью HSM-аппаратных защит.

Если указать этот параметр, параметр *Destination* является необязательным.

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Задает массив операций, которые можно выполнить с помощью ключа, который добавляет этот командлет.
Если этот параметр не указан, может выполняться выполнение всех операций.

Допустимые значения этого параметра — это разделенный запятыми список ключевых операций, заданных [спецификацией JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):

- EFS
- Расшифровки
- Инкапсулирует
- Разтекание
- Рядом
- Подтвержда

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Задает имя ключа, который нужно добавить в хранилище ключей. Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду. Имя должно быть строкой из 1 – 63 знаков длиной, содержащей только 0-9, a-z, A-Z и (дефис).

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Указывает время в виде объекта **DateTime** , до которого невозможно использовать клавишу. Этот параметр использует время в формате UTC. Чтобы получить объект **DateTime** , используйте командлет **Get-Date** . Если этот параметр не указан, клавишу можно использовать сразу.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, к которому этот командлет добавляет ключ. Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.

```yaml
Type: String
Parameter Sets: InteractiveCreate, InteractiveImport
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

### Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Backup-AzureKeyVaultKey](./Backup-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)
