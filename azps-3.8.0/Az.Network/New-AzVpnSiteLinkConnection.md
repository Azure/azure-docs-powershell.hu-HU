---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014323"
---
# <span data-ttu-id="65f99-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="65f99-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="65f99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65f99-102">SYNOPSIS</span></span>
<span data-ttu-id="65f99-103">Azure VpnSiteLinkConnection objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="65f99-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="65f99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65f99-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65f99-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65f99-105">DESCRIPTION</span></span>
<span data-ttu-id="65f99-106">Azure VpnSiteLinkConnection objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="65f99-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="65f99-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65f99-107">EXAMPLES</span></span>

### <span data-ttu-id="65f99-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65f99-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="65f99-109">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy VpnSite, ahol az VpnSiteLinks az Azure-ban, a "testRG" erőforráscsoport az Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="65f99-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="65f99-110">Ezután létrejön egy VPN-átjáró a virtuális központban.</span><span class="sxs-lookup"><span data-stu-id="65f99-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="65f99-111">Miután létrehozta az átjárót, az a New-AzVpnConnection parancs segítségével csatlakozik a VpnSite az VpnSite VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="65f99-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="65f99-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65f99-112">PARAMETERS</span></span>

### <span data-ttu-id="65f99-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="65f99-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="65f99-114">A kapcsolati kapcsolatnak a Mbps-ban való kezeléséhez szükséges sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="65f99-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="65f99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f99-115">-DefaultProfile</span></span>
<span data-ttu-id="65f99-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65f99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f99-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="65f99-117">-EnableBgp</span></span>
<span data-ttu-id="65f99-118">A BGP engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="65f99-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="65f99-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="65f99-119">-IpSecPolicy</span></span>
<span data-ttu-id="65f99-120">Ehhez a kapcsolati kapcsolathoz az IpSec-házirendet kell figyelembe venni.</span><span class="sxs-lookup"><span data-stu-id="65f99-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="65f99-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65f99-121">-Name</span></span>
<span data-ttu-id="65f99-122">név</span><span class="sxs-lookup"><span data-stu-id="65f99-122">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f99-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="65f99-123">-RoutingWeight</span></span>
<span data-ttu-id="65f99-124">Műveletterv vastagsága</span><span class="sxs-lookup"><span data-stu-id="65f99-124">Routing Weight</span></span>

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

### <span data-ttu-id="65f99-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="65f99-125">-SharedKey</span></span>
<span data-ttu-id="65f99-126">A kapcsolat beállításához szükséges megosztott kulcs.</span><span class="sxs-lookup"><span data-stu-id="65f99-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="65f99-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="65f99-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="65f99-128">A kapcsolati kapcsolathoz használja a helyi Azure IP-címet forrás IP-címként.</span><span class="sxs-lookup"><span data-stu-id="65f99-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="65f99-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="65f99-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="65f99-130">Erre a kapcsolati kapcsolatra vonatkozó házirend-alapú forgalom kiválasztók használata</span><span class="sxs-lookup"><span data-stu-id="65f99-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="65f99-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="65f99-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="65f99-132">Átjáró kapcsolódási protokollja: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="65f99-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f99-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="65f99-133">-VpnSiteLink</span></span>
<span data-ttu-id="65f99-134">A VPN-Helykapcsolati objektum csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="65f99-134">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65f99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f99-135">CommonParameters</span></span>
<span data-ttu-id="65f99-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65f99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f99-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65f99-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f99-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65f99-138">INPUTS</span></span>

### <span data-ttu-id="65f99-139">Microsoft. Azure. commands. Network. models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="65f99-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="65f99-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65f99-140">OUTPUTS</span></span>

### <span data-ttu-id="65f99-141">Microsoft. Azure. commands. Network. models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="65f99-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="65f99-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65f99-142">NOTES</span></span>

## <span data-ttu-id="65f99-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65f99-143">RELATED LINKS</span></span>

[<span data-ttu-id="65f99-144">Új – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="65f99-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)