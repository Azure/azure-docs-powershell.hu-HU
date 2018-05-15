# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="b4c52-101">A Microsoft Azure PowerShell 4.0.0 használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="b4c52-102">Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak.</span><span class="sxs-lookup"><span data-stu-id="b4c52-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b4c52-103">Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is.</span><span class="sxs-lookup"><span data-stu-id="b4c52-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="b4c52-104">A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="b4c52-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="b4c52-105">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="b4c52-105">Table of Contents</span></span>

- [<span data-ttu-id="b4c52-106">A Compute-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="b4c52-107">Az EventHub-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="b4c52-108">Az Insights-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="b4c52-109">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="b4c52-110">A ServiceBus-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="b4c52-111">Az SQL-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="b4c52-112">A Storage-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="b4c52-113">A Profile-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="b4c52-114">A Compute-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="b4c52-115">A kiadás a következő kimeneti típusokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="b4c52-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b4c52-116">PSVirtualMachine</span></span>
- <span data-ttu-id="b4c52-117">A `PSVirtualMachine` objektum `DataDiskNames` és `NetworkInterfaceIDs` legfelsőbb szintű tulajdonságai el lettek távolítva a kimenettípusból.</span><span class="sxs-lookup"><span data-stu-id="b4c52-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="b4c52-118">Ezek a tulajdonságok eddig is elérhetőek voltak a `PSVirtualMachine` objektum `StorageProfile` és `NetworkProfile` tulajdonságaiban, és ezentúl csak innen lehet hozzájuk férni.</span><span class="sxs-lookup"><span data-stu-id="b4c52-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="b4c52-119">A módosítás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-119">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="b4c52-120">Az EventHub-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="b4c52-121">A kiadás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="b4c52-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b4c52-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="b4c52-123">A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.</span><span class="sxs-lookup"><span data-stu-id="b4c52-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="b4c52-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b4c52-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="b4c52-125">A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.</span><span class="sxs-lookup"><span data-stu-id="b4c52-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="b4c52-126">Az Insights-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="b4c52-127">A kiadás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="b4c52-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="b4c52-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="b4c52-129">Ez a parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="b4c52-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="b4c52-130">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4c52-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="b4c52-131">A parancsmag kimenete (korábban egy egyetlen objektumból álló lista) egy objektumra módosult; ez az objektum tartalmazza a kérés azonosítóját és az állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="b4c52-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="b4c52-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4c52-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="b4c52-133">Ez a parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="b4c52-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="b4c52-134">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b4c52-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="b4c52-135">A parancsmag kimenetének (egy objektumlistának) az összes eleme egybe lett simítva, azaz a rendszer az objektumokat az `{ Id, Location, Name, Tags, Properties }` struktúra helyett az `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` struktúrával adja vissza, amely magában foglalja egy Azure-erőforrás, valamint egy AlertRuleResource összes legfelsőbb szintű tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="b4c52-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="b4c52-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b4c52-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="b4c52-137">Az `AutoscaleSettingResourceName` mező elavult, mivel az értéke mindig megegyezik a `Name` mező értékével.</span><span class="sxs-lookup"><span data-stu-id="b4c52-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="b4c52-138">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b4c52-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="b4c52-139">A parancsmag kimenete `Boolean` értékről egy `RequestId` és `StatusCode` tulajdonságot tartalmazó objektumra módosul.</span><span class="sxs-lookup"><span data-stu-id="b4c52-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="b4c52-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b4c52-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="b4c52-141">A parancsmag kimenete egy olyan objektumra módosul, amely tartalmazza a kérés azonosítóját és az állapotkódot, valamint a frissített vagy újonnan létrehozott erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b4c52-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
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
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="b4c52-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="b4c52-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="b4c52-143">A parancs új nevet kap: `Update-AzureRmDiagnsoticSettings`</span><span class="sxs-lookup"><span data-stu-id="b4c52-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="b4c52-144">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="b4c52-145">A kiadás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="b4c52-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b4c52-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="b4c52-147">Az `EnableBgp` paraméter értéke `boolean` helyett `string` lett</span><span class="sxs-lookup"><span data-stu-id="b4c52-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="b4c52-148">A ServiceBus-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="b4c52-149">A kiadás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="b4c52-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b4c52-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="b4c52-151">A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.</span><span class="sxs-lookup"><span data-stu-id="b4c52-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="b4c52-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b4c52-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="b4c52-153">A `ResourceGroupName` tulajdonság el lett távolítva a `NamespaceAttributes` kimenettípusból.</span><span class="sxs-lookup"><span data-stu-id="b4c52-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="b4c52-154">Az SQL-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="b4c52-155">A kiadás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="b4c52-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b4c52-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="b4c52-157">A `Tag` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="b4c52-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="b4c52-158">A `GracePeriodWithDataLossHour` paraméter új nevet kapott: `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="b4c52-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="b4c52-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b4c52-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="b4c52-160">A `Tag` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="b4c52-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="b4c52-161">A `GracePeriodWithDataLossHour` paraméter új nevet kapott: `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="b4c52-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="b4c52-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b4c52-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="b4c52-163">A `Tag` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="b4c52-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="b4c52-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b4c52-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="b4c52-165">A `Tag` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="b4c52-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="b4c52-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b4c52-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="b4c52-167">A `PartnerResourceGroupName` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="b4c52-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="b4c52-168">A `PartnerServerName` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="b4c52-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="b4c52-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4c52-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="b4c52-170">A `Usage_Anomaly` érték már nem érvényes az `ExcludedDetectionType` paraméterhez</span><span class="sxs-lookup"><span data-stu-id="b4c52-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="b4c52-171">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4c52-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="b4c52-172">A `Usage_Anomaly` érték már nem érvényes az `ExcludedDetectionType` paraméterhez</span><span class="sxs-lookup"><span data-stu-id="b4c52-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="b4c52-173">A Storage-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="b4c52-174">A kiadás a következő kimenettípus-tulajdonságokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="b4c52-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="b4c52-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="b4c52-176">A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):</span><span class="sxs-lookup"><span data-stu-id="b4c52-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="b4c52-177">A módosítás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="b4c52-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="b4c52-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="b4c52-179">A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):</span><span class="sxs-lookup"><span data-stu-id="b4c52-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="b4c52-180">A módosítás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="b4c52-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="b4c52-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="b4c52-182">A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):</span><span class="sxs-lookup"><span data-stu-id="b4c52-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="b4c52-183">A módosítás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="b4c52-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="b4c52-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="b4c52-185">A következő tulajdonságok lettek eltávolítva a típusból (_megjegyzés_: ezek továbbra is megtalálhatók a `DefaultRequestOptions` tulajdonság alatt):</span><span class="sxs-lookup"><span data-stu-id="b4c52-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="b4c52-186">A módosítás a következő parancsmagokat érinti:</span><span class="sxs-lookup"><span data-stu-id="b4c52-186">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="b4c52-187">A profilparancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="b4c52-188">A kiadás a következő parancsmagokat és a parancsmagok következő kimeneti típusait érintette:</span><span class="sxs-lookup"><span data-stu-id="b4c52-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="b4c52-189">Az Add-AzureRmAccount használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="b4c52-190">Az ```EnvironmentName``` paraméter el lett távolítva, és az ```Environment``` lépett a helyébe. Az ```Environment``` most már egy karakterláncot vesz fel egy ```AzureEnvironment``` objektum helyett.</span><span class="sxs-lookup"><span data-stu-id="b4c52-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="b4c52-191">A Select-AzureRmProfile új nevet kapott: Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b4c52-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="b4c52-192">A ```Select-AzureRmProfile``` új nevet kapott: ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="b4c52-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="b4c52-193">A Save-AzureRmProfile új nevet kapott: Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b4c52-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="b4c52-194">A ```Save-AzureRmProfile``` új nevet kapott: ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="b4c52-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="b4c52-195">A PSAzureContext típusú kimenet használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="b4c52-196">A ```TokenCache``` tulajdonság olyan típusra módosult, amely ```IAzureTokenCache``` elemet implementál ```byte[]``` helyett</span><span class="sxs-lookup"><span data-stu-id="b4c52-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="b4c52-197">A PSAzureAccount típusú kimenet használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="b4c52-198">Az ```AccountType``` tulajdonság a következőre módosult: ```Type```</span><span class="sxs-lookup"><span data-stu-id="b4c52-198">The ```AccountType``` property was changed to ```Type```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="b4c52-199">A PSAzureSubscription típusú kimenet használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="b4c52-200">A ```SubscriptionId``` tulajdonság a következőre módosult: ```Id```</span><span class="sxs-lookup"><span data-stu-id="b4c52-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="b4c52-201">A ```SubscriptionName``` tulajdonság a következőre módosult: ```Name```</span><span class="sxs-lookup"><span data-stu-id="b4c52-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="b4c52-202">A PSAzureTenant típusú kimenet használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="b4c52-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="b4c52-203">A ```TenantId``` tulajdonság a következőre módosult: ```Id```</span><span class="sxs-lookup"><span data-stu-id="b4c52-203">The ```TenantId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="b4c52-204">A ```Domain``` tulajdonság a következőre módosult: ```Directory```</span><span class="sxs-lookup"><span data-stu-id="b4c52-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
