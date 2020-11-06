---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495848"
---
# <span data-ttu-id="032b3-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="032b3-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="032b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="032b3-102">SYNOPSIS</span></span>
<span data-ttu-id="032b3-103">Frissíti a VpnConnection objektumot egy cél állapotra.</span><span class="sxs-lookup"><span data-stu-id="032b3-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="032b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="032b3-104">SYNTAX</span></span>

### <span data-ttu-id="032b3-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="032b3-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="032b3-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="032b3-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="032b3-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="032b3-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="032b3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="032b3-108">DESCRIPTION</span></span>
<span data-ttu-id="032b3-109">Olyan IPSec-kapcsolatot hoz létre, amely összeköti a VpnGateway az RM-ban VpnSite-ként jelölt távoli ügyfél-elágazással.</span><span class="sxs-lookup"><span data-stu-id="032b3-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="032b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="032b3-110">EXAMPLES</span></span>

### <span data-ttu-id="032b3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="032b3-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="032b3-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="032b3-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="032b3-113">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="032b3-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="032b3-114">Miután létrehozta az átjárót, az a New-AzureRmVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="032b3-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="032b3-115">A rendszer ekkor frissíti a kapcsolatot, hogy a Set-AzureRmVpnConnection parancs segítségével új IpSecPolicy legyen.</span><span class="sxs-lookup"><span data-stu-id="032b3-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="032b3-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="032b3-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="032b3-117">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="032b3-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="032b3-118">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="032b3-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="032b3-119">Miután létrehozta az átjárót, az a New-AzureRmVpnConnection parancs segítségével csatlakozik a VpnSite.</span><span class="sxs-lookup"><span data-stu-id="032b3-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="032b3-120">A rendszer ekkor frissíti a kapcsolatot, hogy a biztonságos karakterlánc-összeállítás segítségével új megosztott kulcs legyen.</span><span class="sxs-lookup"><span data-stu-id="032b3-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="032b3-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="032b3-121">PARAMETERS</span></span>

### <span data-ttu-id="032b3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="032b3-122">-AsJob</span></span>
<span data-ttu-id="032b3-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="032b3-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="032b3-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="032b3-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="032b3-125">A kapcsolatnak a Mbps-ban történő kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="032b3-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="032b3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032b3-126">-DefaultProfile</span></span>
<span data-ttu-id="032b3-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="032b3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032b3-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="032b3-128">-EnableBgp</span></span>
<span data-ttu-id="032b3-129">A BGP engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="032b3-129">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="032b3-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="032b3-130">-InputObject</span></span>
<span data-ttu-id="032b3-131">A frissítendő VpnConenction objektum.</span><span class="sxs-lookup"><span data-stu-id="032b3-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="032b3-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="032b3-132">-IpSecPolicy</span></span>
<span data-ttu-id="032b3-133">A kapcsolatnak a Mbps-ban történő kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="032b3-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="032b3-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="032b3-134">-Name</span></span>
<span data-ttu-id="032b3-135">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="032b3-135">The resource name.</span></span>

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

### <span data-ttu-id="032b3-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="032b3-136">-ParentResourceName</span></span>
<span data-ttu-id="032b3-137">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="032b3-137">The parent resource name.</span></span>

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

### <span data-ttu-id="032b3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032b3-138">-ResourceGroupName</span></span>
<span data-ttu-id="032b3-139">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="032b3-139">The resource group name.</span></span>

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

### <span data-ttu-id="032b3-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="032b3-140">-ResourceId</span></span>
<span data-ttu-id="032b3-141">A törlendő VpnConenction-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="032b3-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="032b3-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="032b3-142">-SharedKey</span></span>
<span data-ttu-id="032b3-143">A kapcsolat beállításához szükséges megosztott kulcs.</span><span class="sxs-lookup"><span data-stu-id="032b3-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="032b3-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="032b3-144">-Confirm</span></span>
<span data-ttu-id="032b3-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="032b3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032b3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032b3-146">-WhatIf</span></span>
<span data-ttu-id="032b3-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="032b3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="032b3-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="032b3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032b3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032b3-149">CommonParameters</span></span>
<span data-ttu-id="032b3-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="032b3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032b3-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="032b3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032b3-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="032b3-152">INPUTS</span></span>

### <span data-ttu-id="032b3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="032b3-153">System.String</span></span>

### <span data-ttu-id="032b3-154">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="032b3-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="032b3-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="032b3-155">OUTPUTS</span></span>

### <span data-ttu-id="032b3-156">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="032b3-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="032b3-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="032b3-157">NOTES</span></span>

## <span data-ttu-id="032b3-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="032b3-158">RELATED LINKS</span></span>
