---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: d5f78bf034c46d3b07a97d642032ef0cfe6b339e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159035"
---
# <span data-ttu-id="2c556-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2c556-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="2c556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c556-102">SYNOPSIS</span></span>
<span data-ttu-id="2c556-103">Létrehoz egy Azure VpnSiteLinkConnection objektumot.</span><span class="sxs-lookup"><span data-stu-id="2c556-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="2c556-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c556-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c556-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c556-105">DESCRIPTION</span></span>
<span data-ttu-id="2c556-106">Létrehoz egy Azure VpnSiteLinkConnection objektumot.</span><span class="sxs-lookup"><span data-stu-id="2c556-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="2c556-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c556-107">EXAMPLES</span></span>

### <span data-ttu-id="2c556-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c556-108">Example 1</span></span>
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

<span data-ttu-id="2c556-109">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub és VpnSite, 1 VpnSiteLinks in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="2c556-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="2c556-110">Ezután létrejön egy VPN-átjáró a virtuális központban.</span><span class="sxs-lookup"><span data-stu-id="2c556-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="2c556-111">Miután létrehozta az átjárót, az 1 VpnSiteLinkConnections paranccsal csatlakozik a VpnSite-webhelyhez a New-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="2c556-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="2c556-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c556-112">PARAMETERS</span></span>

### <span data-ttu-id="2c556-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="2c556-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="2c556-114">Az a sávszélesség, amelyet ennek a kapcsolatnak mbps-ként kell kezelnie.</span><span class="sxs-lookup"><span data-stu-id="2c556-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="2c556-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c556-115">-DefaultProfile</span></span>
<span data-ttu-id="2c556-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c556-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c556-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="2c556-117">-EgressNatRule</span></span>
<span data-ttu-id="2c556-118">A kapcsolatkapcsolattal társított, a kigressziós NAT-szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="2c556-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c556-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2c556-119">-EnableBgp</span></span>
<span data-ttu-id="2c556-120">A BGP engedélyezése ehhez a csatolási kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="2c556-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="2c556-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="2c556-121">-IngressNatRule</span></span>
<span data-ttu-id="2c556-122">A kapcsolatkapcsolattal társított bejövő NAT-szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="2c556-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c556-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="2c556-123">-IpSecPolicy</span></span>
<span data-ttu-id="2c556-124">A csatolási kapcsolathoz figyelembe kell venni az IpSec-házirendet.</span><span class="sxs-lookup"><span data-stu-id="2c556-124">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="2c556-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2c556-125">-Name</span></span>
<span data-ttu-id="2c556-126">név</span><span class="sxs-lookup"><span data-stu-id="2c556-126">Name</span></span>

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

### <span data-ttu-id="2c556-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="2c556-127">-RoutingWeight</span></span>
<span data-ttu-id="2c556-128">Routing Weight</span><span class="sxs-lookup"><span data-stu-id="2c556-128">Routing Weight</span></span>

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

### <span data-ttu-id="2c556-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2c556-129">-SharedKey</span></span>
<span data-ttu-id="2c556-130">A kapcsolat beállításához szükséges megosztott kulcs.</span><span class="sxs-lookup"><span data-stu-id="2c556-130">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="2c556-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c556-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="2c556-132">Használja a helyi Azure IP-címet forrás IP-címként ehhez a hivatkozáskapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="2c556-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="2c556-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="2c556-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="2c556-134">Ehhez a kapcsolathoz házirendalapú forgalomválasztókat használjon.</span><span class="sxs-lookup"><span data-stu-id="2c556-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="2c556-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="2c556-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="2c556-136">Átjárókapcsolati protokoll:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="2c556-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="2c556-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2c556-137">-VpnSiteLink</span></span>
<span data-ttu-id="2c556-138">A vpn-webhely hivatkozásobjektuma, amelyhez csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="2c556-138">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="2c556-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c556-139">CommonParameters</span></span>
<span data-ttu-id="2c556-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c556-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c556-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c556-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c556-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c556-142">INPUTS</span></span>

### <span data-ttu-id="2c556-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2c556-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="2c556-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c556-144">OUTPUTS</span></span>

### <span data-ttu-id="2c556-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2c556-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="2c556-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c556-146">NOTES</span></span>

## <span data-ttu-id="2c556-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c556-147">RELATED LINKS</span></span>

[<span data-ttu-id="2c556-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2c556-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)