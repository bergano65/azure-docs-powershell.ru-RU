---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073146"
---
# New-AzStorageAccount

## КРАТКИй обзор
Создание учетной записи хранения.

## Максимальное

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzStorageAccount** создает учетную запись хранения Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание учетной записи хранения
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.

### Пример 2: создание учетной записи хранения BLOB-данных с BlobStorageным и горячим AccessTier
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Эта команда создает учетную запись хранилища BLOB-объектов, которая имеет BlobStorage и горячий AccessTier

### Пример 3: создание учетной записи хранения с помощью StorageV2, создание и назначение удостоверения для Azure KeyVault.
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Эта команда создает учетную запись хранения с StorageV2.  Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.

### Пример 4: создание учетной записи хранения с помощью NetworkRuleSet из JSON
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Эта команда создает учетную запись хранения, которая имеет свойство NetworkRuleSet из JSON.

### Пример 5: создание учетной записи хранения с включенным иерархическое пространством имен.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Эта команда создает учетную запись хранения, для которой включено иерархическое пространство имен.

### Пример 6: создание учетной записи хранения для файлов Azure проверка подлинности в DS и включение больших файловых ресурсов.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Эта команда создает учетную запись хранения с помощью Azure Files Authentication DS и включает большие общие файлы..

### Пример 8. Создание учетной записи хранения с помощью очереди и службы таблиц. Используйте ключ шифрования для учетной записи.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

Эта команда создает учетную запись хранилища, в которой служба очереди и таблица использует ключ шифрования для учетной записи, поэтому очередь и таблица будут использовать один и тот же ключ шифрования с BLOB-объектом и службой файлов. Затем получите доступ к свойствам учетной записи хранения и просмотрите набор шифрования для службы очереди и таблицы.

## ПАРАМЕТРЫ

### -AccessTier
Указывает уровень доступа учетной записи хранения, созданной этим командлетом.
Допустимые значения этого параметра: горячий и крутой.
Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* . Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .

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

### -AsJob
Выполнить командлет в фоновом режиме

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
Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.

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
Указывает имя настраиваемого домена учетной записи хранения.
По умолчанию используется значение Storage.

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

### -EnableAzureActiveDirectoryDomainServicesForFile
Включите проверку подлинности доменных служб Azure Active Directory для учетной записи хранения в Azure Files.

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

### -EnableHierarchicalNamespace
Указывает, включено ли в учетной записи хранения иерархическое пространство имен.

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
Указывает, разрешено ли учетной записи хранения только трафик HTTPS.

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
Указывает, может ли учетная запись хранения поддерживать большие файловые ресурсы размером более 5 TiB. После включения учетной записи эту функцию нельзя отключить. В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетной записи в геоизбыточные учетные записи будет невозможно. Дополнительные сведения https://go.microsoft.com/fwlink/?linkid=2086047

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
Установка KeyType для шифрования в очереди. По умолчанию используется значение Service.
-Account: очередь будет зашифрована с использованием ключа шифрования с областью действия для учетной записи. -Service: очередь всегда будет шифроваться с помощью Service-Managed клавиш. 

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
Задайте для свойства KeyType для таблицы ключ шифрования. По умолчанию используется значение Service.
- Учетная запись: таблица будет зашифрована с использованием ключа шифрования уровня учетной записи. 
- Служба: таблица всегда будет шифроваться с помощью Service-Managed клавиш. 

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

### -Видах
Указывает вариант учетной записи хранения, создаваемой этим командлетом.
Для этого параметра допустимы следующие значения:
- Склад. Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.
- StorageV2. Учетная запись хранения общего назначения версии 2 (GPv2), поддерживающая большие двоичные объекты, таблицы, очереди, файлы и диски, с дополнительными возможностями, такими как уровни данных.
- BlobStorage. Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.
- BlockBlobStorage. Блокировка учетной записи хранения BLOB-объектов, которая поддерживает хранение блочных больших двоичных объектов.
- FileStorage. Учетная запись хранилища файлов, поддерживающая хранение только файлов.
Значением по умолчанию является StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Указывает расположение учетной записи хранения, которую нужно создать.

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

### -Name (имя)
Указывает имя учетной записи хранения, которую нужно создать.

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
NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.

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

### -ResourceGroupName
Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.

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
Указывает имя SKU учетной записи хранения, созданной этим командлетом.
Для этого параметра допустимы следующие значения:
- Standard_LRS. Локально избыточное хранилище.
- Standard_ZRS. Зона — избыточное хранилище.
- Standard_GRS. Геоизбыточное хранилище.
- Standard_RAGRS. Доступное для чтения геоизбыточное хранилище.
- Premium_LRS. Локально — избыточное хранилище Premium.
- Premium_ZRS. Расширенная зона — избыточное хранилище.
- Standard_GZRS геоизбыточной зоны (избыточное хранилище).
- Standard_RAGZRS-для чтения с геоизбыточной зоны (избыточное хранилище).

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

### -Тег
Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере. Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

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
Указывает, нужно ли включить косвенную проверку CName.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
