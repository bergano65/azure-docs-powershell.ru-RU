# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="8453a-101">Критические изменения для Microsoft Azure PowerShell 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8453a-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="8453a-102">Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8453a-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="8453a-103">В каждом разделе описана причина критического изменения и самый простой путь миграции.</span><span class="sxs-lookup"><span data-stu-id="8453a-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="8453a-104">Подробное описание см. в запросах на вытягивание для каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="8453a-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="8453a-105">Оглавление</span><span class="sxs-lookup"><span data-stu-id="8453a-105">Table of Contents</span></span>
1. [<span data-ttu-id="8453a-106">Критические изменения в командлетах Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8453a-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="8453a-107">Критические изменения в командлетах ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8453a-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="8453a-108">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="8453a-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="8453a-109">Критические изменения в командлетах Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8453a-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="8453a-110">В этом выпуске ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="8453a-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="8453a-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="8453a-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="8453a-112">Этот командлет удален и заменен на ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="8453a-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="8453a-113">Старый командлет возвращал сложный объект, представляющий список управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="8453a-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="8453a-114">Новый командлет возвращает простой список записей в ACL для выбранного пути.</span><span class="sxs-lookup"><span data-stu-id="8453a-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="8453a-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="8453a-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="8453a-116">Этим командлетом заменен старый командлет ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span><span class="sxs-lookup"><span data-stu-id="8453a-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="8453a-117">Новый командлет возвращает простой список записей в ACL для выбранного пути с типом ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="8453a-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="8453a-118">Выходные данные этого командлета можно передать в параметр ``-Acl`` для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="8453a-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="8453a-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**.</span><span class="sxs-lookup"><span data-stu-id="8453a-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="8453a-120">Эти командлеты теперь принимают ``DataLakeStoreItemAce[]`` для параметра ``-Acl``.</span><span class="sxs-lookup"><span data-stu-id="8453a-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="8453a-121">``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` возвращает ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="8453a-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="8453a-122">Критические изменения в командлетах ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8453a-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="8453a-123">В этом выпуске ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="8453a-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="8453a-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="8453a-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="8453a-125">Обязательные параметры для ссылки на виртуальную сеть изменены с SubnetName и VnetId на SubnetResourceId в формате ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``.</span><span class="sxs-lookup"><span data-stu-id="8453a-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="8453a-126">**Командлет Set-AzureRmApiManagementVirtualNetworks отмечается как нерекомендуемый**</span><span class="sxs-lookup"><span data-stu-id="8453a-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="8453a-127">Командлет отмечается как нерекомендуемый, так как существует более одного способа задать виртуальную сеть, связанную с развертыванием ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8453a-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="8453a-128">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="8453a-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="8453a-129">В этом выпуске ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="8453a-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="8453a-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="8453a-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="8453a-131">Описание изменений: параметр ``:- Bool parameter:-ActiveActive`` удален и добавлен параметр ``SwitchParameter:-EnableActiveActiveFeature`` для включения функции "активный-активный" при создании шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8453a-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="8453a-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8453a-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="8453a-133">Описание изменений: параметр ``:- Bool parameter:-ActiveActive`` удален и добавлены два параметра ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` для включения и отключения функции "активный-активный" для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8453a-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

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