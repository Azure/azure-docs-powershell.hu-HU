---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154042"
---
# <span data-ttu-id="044d2-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="044d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044d2-102">SYNOPSIS</span></span>
<span data-ttu-id="044d2-103">Frissíti a VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="044d2-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="044d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="044d2-104">SYNTAX</span></span>

### <span data-ttu-id="044d2-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="044d2-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044d2-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="044d2-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="044d2-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="044d2-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044d2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="044d2-108">DESCRIPTION</span></span>
<span data-ttu-id="044d2-109">Az **Update-AzVpnConnection** parancsmag frissíti a VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="044d2-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="044d2-110">A VPN-kapcsolat olyan IPsec-kapcsolatot hoz létre, amely VPN-átjárót csatlakoztat az Azure-ban VPN-webhelyként képviselt távoli ügyfélághoz.</span><span class="sxs-lookup"><span data-stu-id="044d2-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="044d2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="044d2-111">EXAMPLES</span></span>

### <span data-ttu-id="044d2-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="044d2-112">Example 1</span></span>

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

<span data-ttu-id="044d2-113">A fentiekkel létrehozhat egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub és VpnSite in West US in "testRG" resource group in Azure.</span><span class="sxs-lookup"><span data-stu-id="044d2-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="044d2-114">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="044d2-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="044d2-115">Miután létrehozta az átjárót, a virtuális magánhálózathoz csatlakozik a New-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="044d2-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="044d2-116">A kapcsolat ekkor frissül új IpSecPolicy-nak a Set-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="044d2-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="044d2-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="044d2-117">Example 2</span></span>

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

<span data-ttu-id="044d2-118">A fentiekkel létrehozhat egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub és VpnSite in West US in "testRG" resource group in Azure.</span><span class="sxs-lookup"><span data-stu-id="044d2-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="044d2-119">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="044d2-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="044d2-120">Miután létrehozta az átjárót, a virtuális magánhálózathoz csatlakozik a New-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="044d2-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="044d2-121">A rendszer ekkor frissíti a kapcsolatot úgy, hogy a biztonságos karakterlánc-szerkezetet használva új megosztott kulcs legyen.</span><span class="sxs-lookup"><span data-stu-id="044d2-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="044d2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="044d2-122">PARAMETERS</span></span>

### <span data-ttu-id="044d2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="044d2-123">-AsJob</span></span>
<span data-ttu-id="044d2-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="044d2-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="044d2-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="044d2-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="044d2-126">Az a sávszélesség, amelyet a kapcsolatnak mbps-ként kell kezelnie.</span><span class="sxs-lookup"><span data-stu-id="044d2-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="044d2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044d2-127">-DefaultProfile</span></span>
<span data-ttu-id="044d2-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="044d2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="044d2-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="044d2-129">-EnableBgp</span></span>
<span data-ttu-id="044d2-130">A BGP engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="044d2-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="044d2-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="044d2-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="044d2-132">Az internetbiztonság engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="044d2-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="044d2-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="044d2-133">-InputObject</span></span>
<span data-ttu-id="044d2-134">A frissítendve a VpnConnection objektum.</span><span class="sxs-lookup"><span data-stu-id="044d2-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="044d2-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="044d2-135">-IpSecPolicy</span></span>
<span data-ttu-id="044d2-136">Az a sávszélesség, amelyet a kapcsolatnak mbps-ként kell kezelnie.</span><span class="sxs-lookup"><span data-stu-id="044d2-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="044d2-137">-Name</span><span class="sxs-lookup"><span data-stu-id="044d2-137">-Name</span></span>
<span data-ttu-id="044d2-138">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="044d2-138">The resource name.</span></span>

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

### <span data-ttu-id="044d2-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="044d2-139">-ParentResourceName</span></span>
<span data-ttu-id="044d2-140">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="044d2-140">The parent resource name.</span></span>

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

### <span data-ttu-id="044d2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044d2-141">-ResourceGroupName</span></span>
<span data-ttu-id="044d2-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="044d2-142">The resource group name.</span></span>

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

### <span data-ttu-id="044d2-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="044d2-143">-ResourceId</span></span>
<span data-ttu-id="044d2-144">A törölni kívánt VpnConnection-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="044d2-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="044d2-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="044d2-145">-RoutingConfiguration</span></span>
<span data-ttu-id="044d2-146">Útválasztási konfiguráció ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="044d2-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="044d2-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="044d2-147">-SharedKey</span></span>
<span data-ttu-id="044d2-148">A kapcsolat beállításához szükséges megosztott kulcs.</span><span class="sxs-lookup"><span data-stu-id="044d2-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="044d2-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="044d2-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="044d2-150">Csatlakozás kezdeményezése közben használja a helyi Azure IP-címet forráscímként.</span><span class="sxs-lookup"><span data-stu-id="044d2-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="044d2-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="044d2-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="044d2-152">Ehhez a kapcsolathoz házirendalapú forgalomválasztókat használjon.</span><span class="sxs-lookup"><span data-stu-id="044d2-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="044d2-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="044d2-154">A VpnSiteLinkConnections azon listája, amelyekre a VpnConnectionnak szüksége van.</span><span class="sxs-lookup"><span data-stu-id="044d2-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="044d2-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="044d2-155">-Confirm</span></span>
<span data-ttu-id="044d2-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="044d2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044d2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044d2-157">-WhatIf</span></span>
<span data-ttu-id="044d2-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="044d2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044d2-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="044d2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044d2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044d2-160">CommonParameters</span></span>
<span data-ttu-id="044d2-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044d2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044d2-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="044d2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044d2-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="044d2-163">INPUTS</span></span>

### <span data-ttu-id="044d2-164">System.String</span><span class="sxs-lookup"><span data-stu-id="044d2-164">System.String</span></span>

### <span data-ttu-id="044d2-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="044d2-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="044d2-166">OUTPUTS</span></span>

### <span data-ttu-id="044d2-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="044d2-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="044d2-168">NOTES</span></span>

## <span data-ttu-id="044d2-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="044d2-169">RELATED LINKS</span></span>

[<span data-ttu-id="044d2-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="044d2-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="044d2-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="044d2-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="044d2-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="044d2-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
