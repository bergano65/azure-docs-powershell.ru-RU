# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Критические изменения для Microsoft Azure PowerShell 3.0.0

Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.  В каждом разделе описана причина критического изменения и самый простой путь миграции.  Подробное описание см. в запросах на вытягивание для каждого изменения.

## <a name="table-of-contents"></a>Оглавление
1. [Критические изменения в командлетах Data Lake Store](#breaking-changes-to-data-lake-store-cmdlets)
2. [Критические изменения в командлетах ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
3. [Критические изменения в командлетах Network](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Критические изменения в командлетах Data Lake Store

В этом выпуске ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) затронуты следующие командлеты:

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- Этот командлет удален и заменен на ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- Старый командлет возвращал сложный объект, представляющий список управления доступом (ACL). Новый командлет возвращает простой список записей в ACL для выбранного пути.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Этим командлетом заменен старый командлет ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.
- Новый командлет возвращает простой список записей в ACL для выбранного пути с типом ``DataLakeStoreItemAce[]``.
- Выходные данные этого командлета можно передать в параметр ``-Acl`` для следующих командлетов:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**.
- Эти командлеты теперь принимают ``DataLakeStoreItemAce[]`` для параметра ``-Acl``.
- ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` возвращает ``DataLakeStoreItemAce[]``.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Критические изменения в командлетах ApiManagement

В этом выпуске ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) затронуты следующие командлеты:

**New-AzureRmApiManagementVirtualNetwork**
- Обязательные параметры для ссылки на виртуальную сеть изменены с SubnetName и VnetId на SubnetResourceId в формате ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``.

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Командлет Set-AzureRmApiManagementVirtualNetworks отмечается как нерекомендуемый**
- Командлет отмечается как нерекомендуемый, так как существует более одного способа задать виртуальную сеть, связанную с развертыванием ApiManagement.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Критические изменения в командлетах Network

В этом выпуске ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) затронуты следующие командлеты:

**New-AzureRmVirtualNetworkGateway**
- Описание изменений: параметр ``:- Bool parameter:-ActiveActive`` удален и добавлен параметр ``SwitchParameter:-EnableActiveActiveFeature`` для включения функции "активный-активный" при создании шлюза виртуальной сети.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- Описание изменений: параметр ``:- Bool parameter:-ActiveActive`` удален и добавлены два параметра ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` для включения и отключения функции "активный-активный" для шлюза виртуальной сети.

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```