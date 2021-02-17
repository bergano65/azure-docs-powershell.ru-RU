---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217241"
---
# Set-AzStorageAccount

## SYNOPSIS
Изменяет учетную запись хранения.

## СИНТАКСИС

### StorageEncryption (по умолчанию)
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### KeyvaultEncryption
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Set-AzStorageAccount** изменяет учетную запись хранилища Azure.
С помощью этого командлета можно изменить тип учетной записи, обновить домен клиента или настроить теги для учетной записи хранения.

## ПРИМЕРЫ

### Пример 1. Настройка типа учетной записи хранения
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

Эта команда задает для учетной записи хранения Standard_RAGRS.

### Пример 2. Настройка пользовательского домена для учетной записи хранения
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

Эта команда задает настраиваемый домен для учетной записи хранения.

### Пример 3. Настройка уровня доступа
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

Команда задает для уровня Access действительное значение.

### Пример 4. Настройка пользовательского домена и тегов
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

Она задает настраиваемый домен и теги для учетной записи хранения.

### Пример 5. Установите Keyvault в качестве ключевого ключа шифрования
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

Этот набор команд наборов ключей шифрования с новым значением Keyvault.

### Пример 6. Задай для ключей шифрования значение Microsoft.Storage.
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

Этот командный пункт "Ключ шифрования" задает для службы Microsoft.Storage значение "Microsoft.Storage".

### Пример 7. Настройка свойства NetworkRuleSet учетной записи хранения с помощью JSON
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

Эта команда задает свойство NetworkRuleSet учетной записи хранения с помощью JSON

### Пример 8. Получить свойство NetworkRuleSet из учетной записи хранения и настроить его на другую учетную запись хранения
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

Эта первая команда получает свойство NetworkRuleSet из учетной записи хранения, а вторая задает для него другую учетную запись хранения. 

### Пример 9. Обновление учетной записи хранения с помощью kind "Storage" или "BlobStorage" до "StorageV2" вида "Учетная запись хранения"
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

Команда обновит учетную запись хранения с kind "Storage" или "BlobStorage" до "StorageV2" вида "Хранилище".

### Пример 10. Обновление учетной записи хранения путем обеспечения проверки подлинности Azure Files AAD DS.
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

Команда обновляет учетную запись хранения, в результате этого включается проверка подлинности AAD DS для файлов Azure.

### Пример 11. Обновление учетной записи хранения путем вирования проверки подлинности доменной службы Files Active Directory и показа параметра проверки подлинности на основе идентификаторов файлов
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

Команда обновляет учетную запись хранения, в результате чего включается проверка подлинности доменной службы Azure Files Active Directory, а затем показан параметр проверки подлинности на основе удостоверений файлов.

### Пример 12: Set MinimumTlsVersion и AllowBlobPublicAccess
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

Команда задает MinimumTlsVersion и AllowBlobPublicAccess, а затем показывает 2 свойства учетной записи. 

### Пример 13. Обновление учетной записи хранения с помощью параметра RoutingPreference
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

Эта команда обновляет учетную запись хранения с параметром RoutingPreference: PublishMicrosoftEndpoint как false, PublishInternetEndpoint как true и RoutingChoice как MicrosoftRouting.

## PARAMETERS

### -AccessTier
Определяет уровень доступа к учетной записи хранения, которую изменяет этот cmdlet.
Допустимыми значениями для этого параметра являются hot and Cool.
Изменение уровня доступа может привести к дополнительным затратам. Дополнительные сведения см. в хранилище [BLOB-хранилищ Azure: уровни хранилища — "Hot" и "Классный".](http://go.microsoft.com/fwlink/?LinkId=786482)
Если у учетной записи хранения есть Kind as StorageV2 или BlobStorage, вы можете указать параметр *AccessTier.* Если у учетной записи хранения есть kind as Storage, не укажите параметр *AccessTier.*

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
Разрешение или депустив общедоступный доступ ко всем BLOB-данным или контейнерам в учетной записи хранения.

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
Указывает имя пользовательского домена.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
В этой службе можно включить проверку подлинности доменной службы Azure Files Active Directory для учетной записи хранения.

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
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

### -Force
В этом сценарии изменения будут записаны в учетную запись хранения.

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

### -KeyName
Если для шифрования с хранилищем ключей используется шифрование -KeyvaultEncryption, укажите свойство "Имя ключа" с помощью этого параметра.

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyvaultEncryption
Указывает, следует ли использовать ключ KeyVault Microsoft keyVault для ключей шифрования при использовании шифрования службы хранилища. Если параметр KeyName, KeyVersion и KeyVaultUri задан, параметр KeySource будет иметь значение Microsoft.Keyvault независимо от того, задан ли этот параметр. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultUri
При использовании шифрования key Vault путем указания параметра -KeyvaultEncryption используйте этот параметр, чтобы указать URI для хранилища ключей.

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVersion
При использовании шифрования key Vault путем указания параметра -KeyvaultEncryption используйте этот параметр, чтобы указать URI для версии ключа.

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumTlsVersion
Минимальная версия TLS, разрешенная для запросов на хранение.

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
Указывает имя изменяемой учетной записи хранения.

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

### -PublishInternetEndpoint
Указывает на возможность публикации конечных точек хранилища маршрутов в Интернете

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

### -PublishMicrosoftEndpoint
Указывает, должны ли публиковаться конечные точки хранилища маршрутов Майкрософт.

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

### -ResourceGroupName
Указывает имя группы ресурсов, в которой нужно изменить учетную запись хранения.

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

### -RoutingChoice
Выбор маршрутии определяет тип сетевой маршрутии, opted пользователем. Возможные значения: "MicrosoftRouting", "InternetRouting"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
Указывает имя SKU учетной записи хранения.
Допустимыми значениями для этого параметра являются:
- Standard_LRS — локально избыточное хранилище.
- Standard_ZRS — избыточное хранилище зоны.
- Standard_GRS — гео-избыточное хранилище.
- Standard_RAGRS — чтение геообытного хранилища для доступа.
- Premium_LRS — локально избыточное хранилище Premium.
- Standard_GZRS — гео-избыточное хранилище зоны— избыточное хранилище.
- Standard_RAGZRS — чтение доступа к гео-избыточной зоне, избыточный объем хранилища.
Типы учетных Standard_ZRS и Premium_LRS нельзя изменить на другие типы учетных записей.
Другие типы учетных записей нельзя Standard_ZRS или Premium_LRS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEncryption
Указывает, нужно ли использовать ключи, управляемые Майкрософт, для шифрования учетной записи хранения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradeToStorageV2
Обновив учетную запись хранения Kind с Storage или BlobStorage на StorageV2.

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

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[New-AzStorageAccount](./New-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)
