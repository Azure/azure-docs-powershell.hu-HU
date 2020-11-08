---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184051"
---
# <span data-ttu-id="3b2c4-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="3b2c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2c4-103">VPN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="3b2c4-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="3b2c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b2c4-104">SYNTAX</span></span>

### <span data-ttu-id="3b2c4-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b2c4-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b2c4-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="3b2c4-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b2c4-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3b2c4-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b2c4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b2c4-108">DESCRIPTION</span></span>
<span data-ttu-id="3b2c4-109">Az **Update-AzVpnConnection** parancsmag FRISSÍTI a VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="3b2c4-110">A VPN-kapcsolat olyan IPsec-kapcsolatot hoz létre, amely VPN-átjárót létesít egy olyan távoli ügyfél-ágra, amely az Azure-ban VPN-webhelyként képviseli.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="3b2c4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3b2c4-111">EXAMPLES</span></span>

### <span data-ttu-id="3b2c4-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b2c4-112">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="3b2c4-113">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3b2c4-114">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3b2c4-115">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="3b2c4-116">A rendszer ekkor frissíti a kapcsolatot, hogy a Set-AzVpnConnection parancs segítségével új IpSecPolicy legyen.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="3b2c4-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="3b2c4-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="3b2c4-118">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3b2c4-119">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3b2c4-120">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="3b2c4-121">A rendszer ekkor frissíti a kapcsolatot, hogy a biztonságos karakterlánc-összeállítás segítségével új megosztott kulcs legyen.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="3b2c4-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b2c4-122">PARAMETERS</span></span>

### <span data-ttu-id="3b2c4-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b2c4-123">-AsJob</span></span>
<span data-ttu-id="3b2c4-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3b2c4-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3b2c4-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="3b2c4-126">A kapcsolatnak a Mbps-ban való kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2c4-127">-DefaultProfile</span></span>
<span data-ttu-id="3b2c4-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="3b2c4-129">-EnableBgp</span></span>
<span data-ttu-id="3b2c4-130">A BGP engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="3b2c4-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="3b2c4-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="3b2c4-132">Az Internet biztonságának engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="3b2c4-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b2c4-133">-InputObject</span></span>
<span data-ttu-id="3b2c4-134">A frissítendő VpnConnection objektum.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="3b2c4-135">-IpSecPolicy</span></span>
<span data-ttu-id="3b2c4-136">A kapcsolatnak a Mbps-ban való kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b2c4-137">-Name</span></span>
<span data-ttu-id="3b2c4-138">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3b2c4-139">-ParentResourceName</span></span>
<span data-ttu-id="3b2c4-140">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b2c4-141">-ResourceGroupName</span></span>
<span data-ttu-id="3b2c4-142">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b2c4-143">-ResourceId</span></span>
<span data-ttu-id="3b2c4-144">A törlendő VpnConnection-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b2c4-145">-RoutingConfiguration</span></span>
<span data-ttu-id="3b2c4-146">A kapcsolat útválasztási konfigurációja</span><span class="sxs-lookup"><span data-stu-id="3b2c4-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3b2c4-147">-SharedKey</span></span>
<span data-ttu-id="3b2c4-148">A kapcsolat beállításához szükséges megosztott kulcs.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b2c4-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="3b2c4-150">A kapcsolat kezdeményezése közben használja a helyi Azure IP-címet forrás címként.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="3b2c4-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="3b2c4-152">Házirend-alapú forgalom kiválasztók használata ehhez a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="3b2c4-154">Annak a VpnSiteLinkConnections a listája, amelyre a VpnConnection szüksége van.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b2c4-155">-Confirm</span></span>
<span data-ttu-id="3b2c4-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b2c4-157">-WhatIf</span></span>
<span data-ttu-id="3b2c4-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b2c4-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2c4-160">CommonParameters</span></span>
<span data-ttu-id="3b2c4-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b2c4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2c4-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b2c4-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2c4-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b2c4-163">INPUTS</span></span>

### <span data-ttu-id="3b2c4-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3b2c4-164">System.String</span></span>

### <span data-ttu-id="3b2c4-165">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="3b2c4-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b2c4-166">OUTPUTS</span></span>

### <span data-ttu-id="3b2c4-167">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="3b2c4-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b2c4-168">NOTES</span></span>

## <span data-ttu-id="3b2c4-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b2c4-169">RELATED LINKS</span></span>

[<span data-ttu-id="3b2c4-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="3b2c4-171">Új – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="3b2c4-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3b2c4-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="3b2c4-173">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b2c4-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
