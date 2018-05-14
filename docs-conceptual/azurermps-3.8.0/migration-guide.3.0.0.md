# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>A Microsoft Azure PowerShell 3.0.0 használhatatlanná tévő változásai

Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak.  Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is.  A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.

## <a name="table-of-contents"></a>Tartalomjegyzék
1. [A Data Lake Store-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-data-lake-store-cmdlets)
2. [Az ApiManagement-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-apimanagement-cmdlets)
3. [A Network-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>A Data Lake Store-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- A parancsmag el lett távolítva, és a következő lépett a helyébe: ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- A régi parancsmag egy összetett objektumot adott vissza, amely a hozzáférés-vezérlési listát (access control list, ACL) jelölte. Az új parancsmag egy egyszerű, a kiválasztott útvonal ACL-jének bejegyzéseit tartalmazó listát ad vissza.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Ez a parancsmag lép a régi ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` helyébe.
- Az új parancsmag egy egyszerű, a kiválasztott útvonal ACL-jének bejegyzéseit tartalmazó listát ad vissza, és a típusa ``DataLakeStoreItemAce[]``.
- A parancsmag kimenete átadható a következő parancsmagok ``-Acl`` paraméterének:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- Ezek a parancsmagok mostantól elfogadják a ``DataLakeStoreItemAce[]`` értéket a ``-Acl`` paraméterhez.
- A ``DataLakeStoreItemAce[]`` értéket a ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` adja vissza.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Az ApiManagement-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):

**New-AzureRmApiManagementVirtualNetwork**
- A virtuális hálózatra való hivatkozáshoz szükséges paraméterek SubnetName és VnetId helyett SubnetResourceId-re változtak, ebben a formátumban: ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**
- A parancsmag elavult, mivel több módon is be lehetett állítani az ApiManagement üzembe helyezéséhez rendelt virtuális hálózatot.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>A Network-parancsmagok használhatatlanná tévő változásai

A kiadás a következő parancsmagokat érinti ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):

**New-AzureRmVirtualNetworkGateway**
- A ``:- Bool parameter:-ActiveActive`` változás leírása el lett távolítva, és a ``SwitchParameter:-EnableActiveActiveFeature`` hozzá lett adva az aktív-aktív szolgáltatás engedélyezése céljából egy új virtuális hálózati átjáró létrehozása esetén.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- A ``:- Bool parameter:-ActiveActive`` változása leírása el lett távolítva, és két ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` hozzá lett adva az aktív-aktív szolgáltatás engedélyezéséhez és letiltásához a virtuális hálózati átjárókon.

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