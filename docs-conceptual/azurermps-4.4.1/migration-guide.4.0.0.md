# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="a6cbe-101">Критические изменения для Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="a6cbe-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="a6cbe-102">Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a6cbe-103">В каждом разделе описана причина критического изменения и самый простой путь миграции.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="a6cbe-104">Подробное описание см. в запросах на вытягивание для каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="a6cbe-105">Оглавление</span><span class="sxs-lookup"><span data-stu-id="a6cbe-105">Table of Contents</span></span>

- [<span data-ttu-id="a6cbe-106">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="a6cbe-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="a6cbe-107">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="a6cbe-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="a6cbe-108">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="a6cbe-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="a6cbe-109">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="a6cbe-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="a6cbe-110">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6cbe-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="a6cbe-111">Критические изменения в командлетах Sql</span><span class="sxs-lookup"><span data-stu-id="a6cbe-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="a6cbe-112">Критические изменения в командлетах Storage</span><span class="sxs-lookup"><span data-stu-id="a6cbe-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="a6cbe-113">Критические изменения в командлетах Profile</span><span class="sxs-lookup"><span data-stu-id="a6cbe-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="a6cbe-114">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="a6cbe-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="a6cbe-115">В этом выпуске затронуты следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="a6cbe-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6cbe-116">PSVirtualMachine</span></span>
- <span data-ttu-id="a6cbe-117">Свойства верхнего уровня `DataDiskNames` и `NetworkInterfaceIDs` объекта `PSVirtualMachine` удалены из типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="a6cbe-118">Эти свойства всегда были доступны в свойствах `StorageProfile` и `NetworkProfile` объекта `PSVirtualMachine`. Там их можно будет найти и в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="a6cbe-119">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-119">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="a6cbe-120">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="a6cbe-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="a6cbe-121">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="a6cbe-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a6cbe-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="a6cbe-123">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="a6cbe-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a6cbe-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="a6cbe-125">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="a6cbe-126">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="a6cbe-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="a6cbe-127">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="a6cbe-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="a6cbe-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="a6cbe-129">Этот командлет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="a6cbe-130">Remove-AzureRmAlertRule:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="a6cbe-131">Выходные данные этого командлета изменились со списка с одним объектом на один объект. Этот объект включает идентификатор запроса и код состояния.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="a6cbe-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6cbe-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="a6cbe-133">Этот командлет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="a6cbe-134">Get-AzureRmAlertRule:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="a6cbe-135">Каждый элемент выходных данных (список объектов) этого командлета преобразован в плоскую структуру, т. е. вместо возвращения объектов со структурой `{ Id, Location, Name, Tags, Properties }` он будет возвращать объекты со структурой `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`. Она представляет собой все атрибуты Resource в Azure, а также все атрибуты AlertRuleResource верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="a6cbe-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a6cbe-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="a6cbe-137">Поле `AutoscaleSettingResourceName` отмечено как нерекомендуемое, так как его значение всегда совпадало со значением поля `Name`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="a6cbe-138">Remove-AzureRmLogProfile:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="a6cbe-139">Выходные данные командлета изменятся с `Boolean` на объект, содержащий `RequestId` и `StatusCode`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="a6cbe-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a6cbe-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="a6cbe-141">Выходные данные командлета изменятся с объекта, содержащего идентификатор запроса, код состояния и данные обновленного или только что созданного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="a6cbe-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="a6cbe-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="a6cbe-143">Команда будет переименована в `Update-AzureRmDiagnsoticSettings`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="a6cbe-144">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="a6cbe-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="a6cbe-145">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="a6cbe-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a6cbe-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="a6cbe-147">Параметр `EnableBgp` изменен. Теперь он принимает `boolean` вместо `string`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="a6cbe-148">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6cbe-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="a6cbe-149">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="a6cbe-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a6cbe-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="a6cbe-151">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="a6cbe-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a6cbe-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="a6cbe-153">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="a6cbe-154">Критические изменения в командлетах Sql</span><span class="sxs-lookup"><span data-stu-id="a6cbe-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="a6cbe-155">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="a6cbe-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbe-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="a6cbe-157">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="a6cbe-158">Параметр `GracePeriodWithDataLossHour` переименован в `GracePeriodWithDataLossHours`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="a6cbe-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbe-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="a6cbe-160">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="a6cbe-161">Параметр `GracePeriodWithDataLossHour` переименован в `GracePeriodWithDataLossHours`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="a6cbe-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbe-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="a6cbe-163">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="a6cbe-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbe-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="a6cbe-165">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="a6cbe-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbe-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="a6cbe-167">Параметр `PartnerResourceGroupName` удален.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="a6cbe-168">Параметр `PartnerServerName` удален.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="a6cbe-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6cbe-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="a6cbe-170">Значение `Usage_Anomaly` больше не является допустимым для параметра `ExcludedDetectionType`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="a6cbe-171">Set-AzureRmSqlServerThreatDetectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="a6cbe-172">Значение `Usage_Anomaly` больше не является допустимым для параметра `ExcludedDetectionType`.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="a6cbe-173">Критические изменения в командлетах Storage</span><span class="sxs-lookup"><span data-stu-id="a6cbe-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="a6cbe-174">В этом выпуске затронуты следующие свойства типов выходных данных:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="a6cbe-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="a6cbe-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="a6cbe-176">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="a6cbe-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="a6cbe-177">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="a6cbe-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="a6cbe-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="a6cbe-179">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="a6cbe-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="a6cbe-180">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="a6cbe-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="a6cbe-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="a6cbe-182">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="a6cbe-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="a6cbe-183">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="a6cbe-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="a6cbe-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="a6cbe-185">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="a6cbe-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="a6cbe-186">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a6cbe-186">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="a6cbe-187">Критические изменения в командлетах Profile</span><span class="sxs-lookup"><span data-stu-id="a6cbe-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="a6cbe-188">В этом выпуске изменены указанные ниже командлеты и типы выходных данных командлетов.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="a6cbe-189">Критические изменения в AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a6cbe-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="a6cbe-190">Параметр ```EnvironmentName``` удален и заменен на ```Environment```. ```Environment``` теперь принимает строку, а не объект ```AzureEnvironment```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="a6cbe-191">Параметр Select-AzureRmProfile переименован в Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a6cbe-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="a6cbe-192">Параметр ```Select-AzureRmProfile``` переименован в ```Import-AzureRmContext```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="a6cbe-193">Параметр Save-AzureRmProfile переименован в Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a6cbe-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="a6cbe-194">Параметр ```Save-AzureRmProfile``` переименован в ```Save-AzureRmContext```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="a6cbe-195">Критические изменения в типе выходных данных PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a6cbe-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="a6cbe-196">Свойство ```TokenCache``` изменено на тип, реализующий ```IAzureTokenCache``` вместо ```byte[]```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="a6cbe-197">Критические изменения в типе выходных данных PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="a6cbe-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="a6cbe-198">Свойство ```AccountType``` изменено на ```Type```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-198">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="a6cbe-199">Критические изменения в типе выходных данных PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a6cbe-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="a6cbe-200">Свойство ```SubscriptionId``` изменено на ```Id```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="a6cbe-201">Свойство ```SubscriptionName``` изменено на ```Name```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="a6cbe-202">Критические изменения в типе выходных данных PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="a6cbe-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="a6cbe-203">Свойство ```TenantId``` изменено на ```Id```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-203">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="a6cbe-204">Свойство ```Domain``` изменено на ```Directory```.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
