# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="5664c-101">A Microsoft Azure PowerShell 3.0.0 használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="5664c-102">Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak.</span><span class="sxs-lookup"><span data-stu-id="5664c-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="5664c-103">Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is.</span><span class="sxs-lookup"><span data-stu-id="5664c-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="5664c-104">A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="5664c-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5664c-105">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="5664c-105">Table of Contents</span></span>
1. [<span data-ttu-id="5664c-106">A Data Lake Store-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="5664c-107">Az ApiManagement-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="5664c-108">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="5664c-109">A Data Lake Store-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="5664c-110">A kiadás a következő parancsmagokat érinti ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span><span class="sxs-lookup"><span data-stu-id="5664c-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="5664c-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="5664c-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="5664c-112">A parancsmag el lett távolítva, és a következő lépett a helyébe: ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="5664c-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="5664c-113">A régi parancsmag egy összetett objektumot adott vissza, amely a hozzáférés-vezérlési listát (access control list, ACL) jelölte.</span><span class="sxs-lookup"><span data-stu-id="5664c-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="5664c-114">Az új parancsmag egy egyszerű, a kiválasztott útvonal ACL-jének bejegyzéseit tartalmazó listát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="5664c-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="5664c-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="5664c-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="5664c-116">Ez a parancsmag lép a régi ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` helyébe.</span><span class="sxs-lookup"><span data-stu-id="5664c-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="5664c-117">Az új parancsmag egy egyszerű, a kiválasztott útvonal ACL-jének bejegyzéseit tartalmazó listát ad vissza, és a típusa ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="5664c-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="5664c-118">A parancsmag kimenete átadható a következő parancsmagok ``-Acl`` paraméterének:</span><span class="sxs-lookup"><span data-stu-id="5664c-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="5664c-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="5664c-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="5664c-120">Ezek a parancsmagok mostantól elfogadják a ``DataLakeStoreItemAce[]`` értéket a ``-Acl`` paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="5664c-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="5664c-121">A ``DataLakeStoreItemAce[]`` értéket a ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` adja vissza.</span><span class="sxs-lookup"><span data-stu-id="5664c-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="5664c-122">Az ApiManagement-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="5664c-123">A kiadás a következő parancsmagokat érinti ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span><span class="sxs-lookup"><span data-stu-id="5664c-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="5664c-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="5664c-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="5664c-125">A virtuális hálózatra való hivatkozáshoz szükséges paraméterek SubnetName és VnetId helyett SubnetResourceId-re változtak, ebben a formátumban: ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span><span class="sxs-lookup"><span data-stu-id="5664c-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="5664c-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span><span class="sxs-lookup"><span data-stu-id="5664c-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="5664c-127">A parancsmag elavult, mivel több módon is be lehetett állítani az ApiManagement üzembe helyezéséhez rendelt virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="5664c-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="5664c-128">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="5664c-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="5664c-129">A kiadás a következő parancsmagokat érinti ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span><span class="sxs-lookup"><span data-stu-id="5664c-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="5664c-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="5664c-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="5664c-131">A ``:- Bool parameter:-ActiveActive`` változás leírása el lett távolítva, és a ``SwitchParameter:-EnableActiveActiveFeature`` hozzá lett adva az aktív-aktív szolgáltatás engedélyezése céljából egy új virtuális hálózati átjáró létrehozása esetén.</span><span class="sxs-lookup"><span data-stu-id="5664c-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="5664c-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5664c-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="5664c-133">A ``:- Bool parameter:-ActiveActive`` változása leírása el lett távolítva, és két ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` hozzá lett adva az aktív-aktív szolgáltatás engedélyezéséhez és letiltásához a virtuális hálózati átjárókon.</span><span class="sxs-lookup"><span data-stu-id="5664c-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

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