---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324845"
---
# New-AzStorageAccount

## SYNOPSIS
Создает учетную запись хранения.

## СИНТАКСИС

### AzureActiveDirectoryDomainServicesForFile (по умолчанию)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его учетной записью создается** учетная запись хранилища Azure.

## ПРИМЕРЫ

### Пример 1. Создание учетной записи хранения
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Эта команда создает учетную запись хранения для группы ресурсов MyResourceGroup.

### Пример 2. Создание учетной записи хранилища BLOB-хранилищ с помощью BlobStorage Kind и hot AccessTier
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Эта команда создает учетную запись хранилища BLOB-хранилищ, которая с BlobStorage Kind и hot AccessTier

### Пример 3. Создайте учетную запись хранения с помощью Kind StorageV2 и создайте и назначьте удостоверение для Azure KeyVault.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Эта команда создает учетную запись хранения с kind StorageV2.  Кроме того, оно создает и назначает удостоверение, которое можно использовать для управления ключами учетных записей с помощью ключей Azure KeyVault.

### Пример 4. Создание учетной записи хранения с помощью NetworkRuleSet из JSON
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Эта команда создает учетную запись хранения с свойством NetworkRuleSet из JSON.

### Пример 5. Создание учетной записи хранения с включенной иерархической областью имен.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Эта команда создает учетную запись хранения с включенной иерархической областью имен.

### Пример 6. Создание учетной записи хранения с помощью проверки подлинности AAD DS Azure и использование большой папки с файлами.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Эта команда создает учетную запись хранения с проверкой подлинности azure Files AAD DS и включает большой объем файловой папки.

### Пример 7. Создайте учетную запись хранения с возможностью проверки подлинности доменной службы Files Active Directory.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Эта команда создает учетную запись хранения с проверкой подлинности доменной службы Active Directory "Файлы Active Directory".

### Пример 8. Создайте учетную запись хранения с помощью очереди и службы таблиц с помощью ключа шифрования уровня учетной записи и обязательного шифрования инфраструктуры.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

Эта команда создает учетную запись хранения с очереди, а табличные службы используют ключ шифрования уровня учетной записи и требуют шифрования инфраструктуры, поэтому для очереди и таблицы будет применяться один и тот же ключ шифрования для BLOB-объектов и файловой службы, а служба приместит дополнительный уровень шифрования с управляемыми платформой ключами для неавторятельных данных.
Затем получите свойства учетной записи хранения и просмотреть тип ключа шифрования очереди и табличная служба и значение RequireInfrastructureEncryption.

### Пример 9. Создание учетной записи MinimumTlsVersion и AllowBlobPublicAccess
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

Команда для создания учетной записи с minimumTlsVersion и AllowBlobPublicAccess, а затем показать 2 свойства созданной учетной записи 

## PARAMETERS

### -AccessTier
Определяет уровень доступа к учетной записи хранения, которую создает этот cmdlet.
Допустимыми значениями для этого параметра являются hot и Cool.
Если для параметра *Kind* указано значение BlobStorage, необходимо указать значение *параметра AccessTier.* Если для этого параметра Kind задан параметр *Storage,* не укажите параметр *AccessTier.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryAzureStorageSid
Определяет идентификатор безопасности для хранилища Azure. Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
Определяет GUID домена. Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
Определяет основной домен, для который является полномочного DNS-сервером AD. Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
Идентификатор безопасности (SID). Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
Указывает лес Active Directory, который нужно получить. Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetBiosDomainName
Указывает доменное имя NetBIOS. Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBlobPublicAccess
Разрешить общедоступный доступ ко всем BLOB-контейнерам в учетной записи хранения. Для этого свойства по умолчанию верно верное толкование.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Запуск cmdlet в фоновом режиме

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

### -AssignIdentity
Создание и назначение удостоверения учетной записи хранения для этой учетной записи хранения для использования с основными службами управления, например Azure KeyVault.

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

### -CustomDomainName
Указывает имя пользовательского домена учетной записи хранения.
Значение по умолчанию — "Хранилище".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EnableActiveDirectoryDomainServicesForFile
В этой службе можно включить проверку подлинности доменной службы Azure Files Active Directory для учетной записи хранения.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
В этой области можно включить проверку подлинности доменной службы Azure Active Directory для учетной записи хранения.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
Указывает, включает ли учетная запись хранения иерархическое пространство имен.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Указывает, включает ли учетная запись хранения только трафик HTTPS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
Указывает, поддерживает ли учетная запись хранения большие папки емкостью более 5 ТБ. После включения учетной записи эту функцию невозможно отключить. В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетных записей в геоизбыточные учетные записи невозможно. Подробнее в https://go.microsoft.com/fwlink/?linkid=2086047

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

### -EncryptionKeyTypeForQueue
За установите keyType шифрования для очереди. Значение по умолчанию — Service (Служба).
-Account: Очередь шифруется с помощью ключа шифрования на уровнях учетной записи. -Service: Очередь всегда шифруется с Service-Managed клавиш. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
За установите ключ шифрования для таблицы. Значение по умолчанию — Service (Служба).
- Учетная запись: таблица будет зашифрована с помощью ключа шифрования уровня учетной записи. 
- Служба: таблица всегда шифруется с Service-Managed клавиш. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Определяет тип учетной записи хранения, которую создает этот cmdlet.
Допустимые значения этого параметра:
- "Хранилище". Учетная запись хранения общего назначения, которая поддерживает хранение BLOB-файлов, таблиц, очередей, файлов и дисков.
- StorageV2. Учетная запись хранения общего назначения версии 2 (GPv2), которая поддерживает большие большие объекты, таблицы, очереди, файлы и диски, с расширенными возможностями, например переучетом данных.
- BlobStorage. Учетная запись хранилища BLOB-хранилищ, которая поддерживает хранение только BLOB-хранилищ.
- BlockBlobStorage. Блокировать учетную запись хранилища BLOB-блоков, которая поддерживает только хранение блоков BLOB-блоков.
- FileStorage. Учетная запись хранилища файлов, которая поддерживает только хранение файлов.
Значение по умолчанию — StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Определяет расположение создаемой учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
Минимальная версия TLS, разрешенная для запросов на хранение. По умолчанию для этого свойства закончится значение TLS 1.0.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя создаемой учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для определения значений сетевых свойств, таких как службы, разрешенные для обхода правил, и обработки запросов, которые не соответствуют ни одной из них.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireInfrastructureEncryption
Служба будет применять дополнительный уровень шифрования с управляемыми платформой ключами для неавторяых данных.

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

### -ResourceGroupName
Имя группы ресурсов, в которую нужно добавить учетную запись хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Указывает SKU учетной записи хранения, которую создает этот cmdlet.
Допустимые значения этого параметра:
- Standard_LRS. Локальное избыточное хранилище.
- Standard_ZRS. Избыточное хранилище зоны.
- Standard_GRS. Гео избыточный объем хранилища.
- Standard_RAGRS. Чтение геобытного хранилища в Access.
- Premium_LRS. "Премиум" — локально избыточное хранилище.
- Premium_ZRS. Premium zone-redundant storage.
- Standard_GZRS — гео-избыточное хранилище зоны— избыточное хранилище.
- Standard_RAGZRS — чтение доступа к гео-избыточной зоне, избыточный объем хранилища.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Пары значений ключа в виде hash table set as tags (Теги на сервере). Например: @{key0="value0";key1=$null;key2="value2"}

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

### -UseSubDomain
Указывает, следует ли включить непрямую проверку CName.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
