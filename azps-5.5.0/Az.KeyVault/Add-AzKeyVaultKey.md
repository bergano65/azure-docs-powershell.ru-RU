---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 61125ae7d9fa78ec9f121cc9b60610258ad2c67c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405403"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Создает ключ в хранилище ключей или импортирует его в хранилище ключей.

## СИНТАКСИС

### InteractiveCreate (по умолчанию)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveCreate
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveImport
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectCreate
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectImport
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdCreate
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdImport
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **его** использованием можно создать ключ в хранилище ключей Azure или импортировать его в хранилище ключей.
Используйте этот cmdlet для добавления клавиш, используя один из следующих способов:
- Создайте ключ в модуле безопасности оборудования (HSM) в службе key Vault.
- Создайте ключ в программном обеспечении в службе key Vault.
- Импортировать ключ из собственного модуля безопасности оборудования (HSM) в HSMs в службе key Vault.
- Импортировать ключ из PFX-файла на компьютере.
- Импортировать ключ из PFX-файла на компьютере в аппаратные модули безопасности (HSMs) в службе key Vault.
Для любой из этих операций можно уписать ключевые атрибуты или принять параметры по умолчанию.
При создании или импорте ключа, который имеет то же имя, что и у существующего ключа в хранилище ключей, исходный ключ обновляется с помощью значений, которые вы указываете для нового ключа. Для доступа к предыдущим значениям можно использовать URI для конкретной версии ключа. Чтобы узнать о ключевых версиях и [](http://go.microsoft.com/fwlink/?linkid=518560) структуре URI, см. документацию по ключевому сейфу REST API "Ключи и секрет".
Примечание. Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением byok file name) с помощью инструмента "Хранилище ключей Azure BYOK". Дополнительные сведения см. в сведениях о том, как создавать и [HSM-Protected ключей для хранилища ключей Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)
Лучше всего создать или обновить ключ с помощью Backup-AzKeyVaultKey управления. Функции отменить невозможно, поэтому если вы случайно удалили или удалили ключ, а затем передумали, его невозможно восстановить, если у вас нет резервной копии, которую вы сможете восстановить.

## ПРИМЕРЫ

### Пример 1. Создание ключа
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Эта команда создает защищенный программным обеспечением ключ ITSoftware в хранилище с именем Contoso.

### Пример 2. Создание защищенного HSM ключа
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Эта команда создает ключ, защищенный HSM, в хранилище с именем Contoso.

### Пример 3. Создание ключа со значениями, которые не являются значениями по умолчанию
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Первая команда сохраняет значения в переменной "$KeyOperations".
Вторая команда создает объект **даты** и времени, определенный в UTC, с помощью командлета **Get-Date.**
Этот объект определяет время на два года в будущем. Эта команда сохраняет эту дату в переменной $Expires. Для получения дополнительных сведений введите `Get-Help Get-Date` .
Третья команда создает объект **даты и времени** с помощью командлета **Get-Date.** Этот объект указывает текущее время в UTC. Эта команда сохраняет эту дату в переменной $NotBefore.
Конечная команда создает ключ с именем ITHsmNonDefault, защищенный HSM. Команда определяет значения для разрешенных операций ключа, хранимых $KeyOperations. Команда определяет время параметров *Expires* (Срок действия) и *NotBefore,* созданных в предыдущих командах, и тегов для высокой важности и ИТ-параметров. Новый ключ отключен. Вы можете включить его с помощью **cmdlet Set-AzKeyVaultKey.**

### Пример 4. Импорт ключа, защищенного HSM
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Эта команда импортирует ключ "ITByok" из расположения, заданного *параметром KeyFilePath.* Импортируемый ключ является ключом, защищенным HSM.
Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением имени файла BYOK) с помощью средства BYOK key Vault Azure.
Дополнительные сведения см. в сведениях о том, как создавать и [HSM-Protected ключей для хранилища ключей Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)

### Пример 5. Импорт ключа, защищенного программным обеспечением
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Password строке. Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .
Вторая команда создает пароль программного обеспечения в хранилище ключей Contoso. Команда определяет расположение ключа и пароля, которые хранятся в $Password.

### Пример 6. Импорт ключа и назначение атрибутов
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Password строке.
Вторая команда создает объект **даты** и времени с помощью командлета **Get-Date,** а затем сохраняет его в $Expires переменной.
Третья команда создает переменную $tags, чтобы настроить теги для высокой важности и ИТ-информации.
Конечная команда импортирует ключ как клавишу HSM из указанного расположения. Команда определяет срок действия, которые хранятся $Expires пароль, которые хранятся в $Password, и применяет теги, хранимые в $tags.

### Пример 7. Создание ключа Exchange (KEK) для функции "создать собственный ключ" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Создает ключ (ключ обмена ключом). КЕК должен быть ключом RSA-HSM, который имеет только операцию импорта. Только ключ сейфа Premium SKU поддерживает ключи RSA-HSM.
Дополнительные сведения https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## PARAMETERS

### -CurveName
Определяет имя кривой шифрования с многотипной кривой. Это значение допустимо, если KeyType — EC.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Destination
Указывает, следует ли добавить ключ в качестве защищенного по программному обеспечению или защищенного HSM ключа в службе key Vault.
Допустимые значения: HSM и Программное обеспечение.
Примечание. Чтобы использовать HSM в качестве назначения, у вас должен быть ключ сейф, который поддерживает HSMs. Дополнительные сведения об уровнях обслуживания и возможностях хранилища ключей Azure см. на веб-сайте цены [на ключ хранилища Azure.](http://go.microsoft.com/fwlink/?linkid=512521)
Этот параметр требуется при создании нового ключа. Если вы импортируете ключ с помощью *параметра KeyFilePath,* этот параметр является необязательным:
- Если этот параметр не задан и этот cmdlet импортирует ключ с расширением byok, он будет импортироваться как ключ, защищенный HSM. Этот ключ нельзя импортировать как защищенный программным обеспечением ключ.
- Если этот параметр не указан, а этот cmdlet импортирует ключ с расширением имени файла PFX, ключ будет импортироваться как защищенный программным обеспечением ключ.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Указывает на то, что для добавляемого ключа за установлено начальное состояние отключения. Любая попытка использовать ключ будет со сбой. Используйте этот параметр, если вы предварительно добавили ключи, которые предполагается включить позже.

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

### -Expires
Срок действия ключа, который добавляет этот **cmdlet,** определяет срок действия в качестве объекта даты и времени. Этот параметр использует UTC. Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.** Для получения дополнительных сведений введите `Get-Help Get-Date` . Если этот параметр не задан, срок действия ключа не истекает.

```yaml
Type: System.Nullable`1[System.DateTime]
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
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmObject
Объект HSM.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HsmResourceId
ИД ресурса HSM.

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Объект Vault.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Пароль импортируемого файла в качестве объекта **SecureString.** Чтобы получить объект **SecureString,** используйте **cmdlet ConvertTo-SecureString.** Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` . Этот пароль необходимо указать для импорта файла с расширением PFX.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Путь к локальному файлу, который содержит ключевые материалы, импортируемые этим cmdlet.
Допустимые расширения имен файлов: BYOK и PFX.
- Если это BYOK-файл, он автоматически защищен HSMs после импорта, и этот элемент по умолчанию нельзя переопрестить.
- Если это PFX-файл, ключ автоматически защищен программным обеспечением после импорта. Чтобы переопререгировать этот параметр по умолчанию, задате для параметра *Destination* параметр HSM так, чтобы ключ защищен HSM.
Если этот параметр указан, параметр *Destination* является необязательным.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Определяет массив операций, которые можно выполнять с помощью ключа, который добавляет этот cmdlet.
Если этот параметр не задан, можно выполнить все операции.
Допустимыми значениями для этого параметра является список операций, разделенных запятыми, в соответствии со спецификацией [JSON Web Key (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)
- шифровать
- расшифровать
- wrapKey
- unw уберегатьKey
- подписать
- проверить
- импорт (только для KEK, см. пример 7)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Определяет тип ключа этого ключа. При импорте ключей BYOK по умолчанию за счет RSA.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя ключа, который нужно добавить в хранилище. Этот cmdlet конструирует полное доменное имя (FQDN) ключа на основе имени, указанного этим параметром, имени хранилища ключа и текущей среды. Имя должно быть строкой от 1 до 63 символов длины, которая содержит только 0–9, a-z, A-Z и - (символ тире).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Время в качестве объекта **даты и времени,** перед которым нельзя использовать ключ. Этот параметр использует UTC. Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.** Если этот параметр не задан, его можно использовать сразу же.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ИД ресурса хранилища.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
Размер ключа RSA в битах. Если не указано, служба предоставит безопасный стандартный стандарт.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Пары значений ключа в виде hash table. Например: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, к которому этот cmdlet добавляет ключ. Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

