# <a name="table-of-contents"></a>Оглавление
1. [Удаление параметров Force](#removal-of-force-parameters)
2. [Изменение параметров Tag](#change-of-tag-parameters)
3. [Критические изменения в командлетах Storage](#breaking-changes-to-storage-cmdlets)
4. [Критические изменения в командлетах AD](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a>Удаление параметров Force

В этом выпуске мы удалили все устаревшие параметры `Force` из командлетов и соответствующие предупреждения о том, что параметры будут удалены в следующем выпуске.

Это изменение затрагивает следующие командлеты:

**ApiManagement**
- Remove-AzureRmApiManagement
- Remove-AzureRmApiManagementApi
- Remove-AzureRmApiManagementGroup
- Remove-AzureRmApiManagementLogger
- Remove-AzureRmApiManagementOpenIdConnectProvider
- Remove-AzureRmApiManagementOperation
- Remove-AzureRmApiManagementPolicy
- Remove-AzureRmApiManagementProduct
- Remove-AzureRmApiManagementProperty
- Remove-AzureRmApiManagementSubscription
- Remove-AzureRmApiManagementUser

**Автоматизация**
- Remove-AzureRmAutomationCertificate
- Remove-AzureRmAutomationCredential
- Remove-AzureRmAutomationVariable
- Remove-AzureRmAutomationWebhook

**Пакетная служба**
- Remove-AzureBatchCertificate
- Remove-AzureBatchComputeNode
- Remove-AzureBatchComputeNodeUser

**DataFactories**
- Resume-AzureRmDataFactoryPipeline
- Set-AzureRmDataFactoryPipelineActivePeriod
- Suspend-AzureRmDataFactoryPipeline

**DataLakeStore**
- Remove-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemAcl
- Set-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemOwner

**OperationalInsights**
- Remove-AzureRmOperationalInsightsSavedSearch

**Профиль**
- Remove-AzureRmEnvironment

**Кэш Redis**
- Remove-AzureRmRedisCacheDiagnostics

**Ресурсы**
- Register-AzureRmProviderFeature
- Register-AzureRmResourceProvider
- Remove-AzureRmADServicePrincipal
- Remove-AzureRmPolicyAssignment
- Remove-AzureRmResourceGroupDeployment
- Remove-AzureRmRoleAssignment
- Stop-AzureRmResourceGroupDeployment
- Unregister-AzureRmResourceProvider

**Хранилище**
- Remove-AzureStorageContainerStoredAccessPolicy
- Remove-AzureStorageQueueStoredAccessPolicy
- Remove-AzureStorageShareStoredAccessPolicy
- Remove-AzureStorageTableStoredAccessPolicy

**StreamAnalytics**
- Remove-AzureRmStreamAnalyticsFunction
- Remove-AzureRmStreamAnalyticsInput
- Remove-AzureRmStreamAnalyticsJob
- Remove-AzureRmStreamAnalyticsOutput

**Tag**
- Remove-AzureRmTag

<br>

Если в вашем скрипте используется любой указанный выше командлет, можно применить критическое изменение, просто удалив параметр `Force`.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a>Изменение параметров Tag

В этом выпуске имя параметра `Tags` изменено на `Tag`, а тип изменен с `Hashtable[]` на `Hashtable`, что преобразовало формат пар "ключ-значение".

Ранее каждая запись в `Hashtable[]` представляла одну пара "ключ-значение":

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

Теперь `Name` и `Value` больше не нужны. Это позволяет создавать пары "ключ-значение", назначив `Key = "Value"` в `Hashtable`:

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

Это изменение затрагивает следующие командлеты:

**Пакетная служба**
- Get-AzureRmBatchAccount
- New-AzureRmBatchAccount
- Set-AzureRmBatchAccount

**Среда выполнения приложений**
- New-AzureRmVM
- Update-AzureRmVM

**DataLakeAnalytics**
- New-AzureRmDataLakeAnalyticsAccount
- Set-AzureRmDataLakeAnalyticsAccount

**DataLakeStore**
- New-AzureRmDataLakeStoreAccount
- Set-AzureRmDataLakeStoreAccount

**Dns**
- New-AzureRmDnsZone
- Set-AzureRmDnsZone

**Хранилище ключей**
- Get-AzureRmKeyVault
- New-AzureRmKeyVault

**Сеть**
- New-AzureRmApplicationGateway
- New-AzureRmExpressRouteCircuit
- New-AzureRmLoadBalancer
- New-AzureRmLocalNetworkGateway
- New-AzureRmNetworkInterface
- New-AzureRmNetworkSecurityGroup
- New-AzureRmPublicIpAddress
- New-AzureRmRouteTable
- New-AzureRmVirtualNetwork
- New-AzureRmVirtualNetworkGateway
- New-AzureRmVirtualNetworkGatewayConnection
- New-AzureRmVirtualNetworkPeering.

**Ресурсы**
- Find-AzureRmResource
- Find-AzureRmResourceGroup
- New-AzureRmResource;
- New-AzureRmResourceGroup
- Set-AzureRmResource.
- Set-AzureRmResourceGroup

**SQL**
- New-AzureRmSqlDatabase
- New-AzureRmSqlDatabaseCopy
- New-AzureRmSqlDatabaseSecondary
- New-AzureRmSqlElasticPool
- New-AzureRmSqlServer
- Set-AzureRmSqlDatabase
- Set-AzureRmSqlElasticPool
- Set-AzureRmSqlServer

**Хранилище**
- New-AzureRmStorageAccount;
- Set-AzureRmStorageAccount.

**TrafficManager**
- New-AzureRmTrafficManagerProfile

<br>

Если в вашем скрипте используется любой указанный выше командлет, можно применить критическое изменение, изменив параметр `Tags` на `Tag`, а также преобразовав `Tag` в новый формат.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a>Критические изменения в командлетах Storage

В этом выпуске затронуты следующие командлеты:

**Get-AzureRmStorageAccountKey**
- Командлет возвращает список ключей, а не объект со свойствами для каждого ключа

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

**New-AzureRmStorageAccountKey**
- Поле `StorageAccountRegenerateKeyResponse` в выходных данных командлета переименовано в `StorageAccountListKeysResults`, которое теперь является списком ключей, а не объектом со свойствами для каждого ключа.

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

**New/Get/Set-AzureRmStorageAccount**
- Поле `AccountType` в выходных данных этого командлета переименовано в `Sku.Name`.
- Тип выходных данных первичных и вторичных конечных точек для больших двоичных объектов, таблиц, очередей и файлов изменен с `Uri` на `String`.

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a>Критические изменения в командлетах AD

В этом выпуске затронуты следующие командлеты:

**Get-AzureRMADServicePrincipal**
- Поле `ServicePrincipalName` в выходных данных этого командлета переименовано в `ServicePrincipalNames` и теперь является коллекцией. Теперь `ApplicationId` отображается также как одно из имен субъекта-службы с identifierUri.

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

**Get-AzureRmADApplication**
- Параметр `ApplicationObjectId` переименован в `ObjectId`.
- В выходных данных этого командлета поле `ApplicationObjectId` переименовано в `ObjectId`.

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

**Remove-AzureRmADApplication**
- Параметр `ApplicationObjectId` переименован в `ObjectId`.

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

**New-AzureRmADApplication**
- В выходных данных этого командлета поле `ApplicationObjectId` переименовано в `ObjectId`.
- Удалены параметры `KeyValue`, `KeyUsage` и `KeyType`.

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

**Get-AzureRmADGroup**
- Поле `Mail` удалено из выходных данных.

**Get-AzureRmADUser**
- Поле `Mail` удалено из выходных данных.

**New-AzureRmADServicePrincipal**
- Удален параметр `DisableAccount`.

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```