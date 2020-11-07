---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669922"
---
# <span data-ttu-id="bb0c0-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb0c0-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="bb0c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0c0-103">VPN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="bb0c0-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="bb0c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb0c0-104">SYNTAX</span></span>

### <span data-ttu-id="bb0c0-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb0c0-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb0c0-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="bb0c0-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb0c0-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="bb0c0-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb0c0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb0c0-108">DESCRIPTION</span></span>
<span data-ttu-id="bb0c0-109">Az **Update-AzVpnConnection** parancsmag FRISSÍTI a VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="bb0c0-110">A VPN-kapcsolat olyan IPsec-kapcsolatot hoz létre, amely VPN-átjárót létesít egy olyan távoli ügyfél-ágra, amely az Azure-ban VPN-webhelyként képviseli.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="bb0c0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bb0c0-111">EXAMPLES</span></span>

### <span data-ttu-id="bb0c0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb0c0-112">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="bb0c0-113">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="bb0c0-114">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="bb0c0-115">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="bb0c0-116">A rendszer ekkor frissíti a kapcsolatot, hogy a Set-AzVpnConnection parancs segítségével új IpSecPolicy legyen.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="bb0c0-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="bb0c0-117">Example 2</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="bb0c0-118">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="bb0c0-119">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="bb0c0-120">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="bb0c0-121">A rendszer ekkor frissíti a kapcsolatot, hogy a biztonságos karakterlánc-összeállítás segítségével új megosztott kulcs legyen.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="bb0c0-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb0c0-122">PARAMETERS</span></span>

### <span data-ttu-id="bb0c0-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb0c0-123">-AsJob</span></span>
<span data-ttu-id="bb0c0-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bb0c0-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb0c0-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="bb0c0-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="bb0c0-126">A kapcsolatnak a Mbps-ban történő kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0c0-127">-DefaultProfile</span></span>
<span data-ttu-id="bb0c0-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb0c0-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="bb0c0-129">-EnableBgp</span></span>
<span data-ttu-id="bb0c0-130">A BGP engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="bb0c0-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="bb0c0-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb0c0-131">-InputObject</span></span>
<span data-ttu-id="bb0c0-132">A frissítendő VpnConenction objektum.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-132">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="bb0c0-133">-IpSecPolicy</span></span>
<span data-ttu-id="bb0c0-134">A kapcsolatnak a Mbps-ban történő kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb0c0-135">-Name</span></span>
<span data-ttu-id="bb0c0-136">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-136">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bb0c0-137">-ParentResourceName</span></span>
<span data-ttu-id="bb0c0-138">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-138">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb0c0-139">-ResourceGroupName</span></span>
<span data-ttu-id="bb0c0-140">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb0c0-141">-ResourceId</span></span>
<span data-ttu-id="bb0c0-142">A törlendő VpnConenction-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-142">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="bb0c0-143">-SharedKey</span></span>
<span data-ttu-id="bb0c0-144">A kapcsolat beállításához szükséges megosztott kulcs.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-144">The shared key required to set this connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb0c0-145">-Confirm</span></span>
<span data-ttu-id="bb0c0-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb0c0-147">-WhatIf</span></span>
<span data-ttu-id="bb0c0-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb0c0-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb0c0-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0c0-150">CommonParameters</span></span>
<span data-ttu-id="bb0c0-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb0c0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0c0-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb0c0-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0c0-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb0c0-153">INPUTS</span></span>

### <span data-ttu-id="bb0c0-154">System. String</span><span class="sxs-lookup"><span data-stu-id="bb0c0-154">System.String</span></span>

### <span data-ttu-id="bb0c0-155">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb0c0-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="bb0c0-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb0c0-156">OUTPUTS</span></span>

### <span data-ttu-id="bb0c0-157">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb0c0-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="bb0c0-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb0c0-158">NOTES</span></span>

## <span data-ttu-id="bb0c0-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb0c0-159">RELATED LINKS</span></span>

[<span data-ttu-id="bb0c0-160">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb0c0-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="bb0c0-161">Új – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb0c0-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="bb0c0-162">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb0c0-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
