---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354857"
---
# <span data-ttu-id="f21b2-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f21b2-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f21b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f21b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f21b2-103">Létrehoz egy új társviszony-konfigurációt, amely hozzáadódik egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="f21b2-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f21b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f21b2-104">SYNTAX</span></span>

### <span data-ttu-id="f21b2-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f21b2-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f21b2-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="f21b2-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f21b2-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="f21b2-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f21b2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f21b2-108">DESCRIPTION</span></span>
<span data-ttu-id="f21b2-109">A **New-AzExpressRouteCircuitPeeringConfig** parancsmag társviszony-konfigurációt ad egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="f21b2-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="f21b2-110">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz.</span><span class="sxs-lookup"><span data-stu-id="f21b2-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="f21b2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f21b2-111">EXAMPLES</span></span>

### <span data-ttu-id="f21b2-112">1. példa: Új ExpressRoute-áramkör létrehozása társviszony-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="f21b2-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="f21b2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f21b2-113">PARAMETERS</span></span>

### <span data-ttu-id="f21b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21b2-114">-DefaultProfile</span></span>
<span data-ttu-id="f21b2-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f21b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f21b2-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="f21b2-116">-LegacyMode</span></span>
<span data-ttu-id="f21b2-117">A társviszony-létesítés régi módja</span><span class="sxs-lookup"><span data-stu-id="f21b2-117">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-118">-MicrosoftConfigAdvertedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="f21b2-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="f21b2-119">A MicrosoftPeering társviszony-típusa esetében meg kell adnia a BGP-munkameneten keresztül meghirdetni tervezhető előtagok listáját.</span><span class="sxs-lookup"><span data-stu-id="f21b2-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="f21b2-120">Csak a nyilvános IP-cím előtagokat fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f21b2-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="f21b2-121">Vesszővel elválasztott listát is küldhet, ha előtagokat tervez küldeni.</span><span class="sxs-lookup"><span data-stu-id="f21b2-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="f21b2-122">Ezeket az előtagokat a Routing Registry Name (RIR/IRR) névben kell regisztrálnia.</span><span class="sxs-lookup"><span data-stu-id="f21b2-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="f21b2-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="f21b2-124">Ha Ön olyan hirdetési előtagokat ad meg, amelyek nem a társviszony-létesítő AS számhoz vannak regisztrálva, megadhatja azt az AS-számot, amelyre regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="f21b2-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="f21b2-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="f21b2-126">A routing registry name (RIR /BRR), amelyre az AS szám és az előtagok regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="f21b2-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f21b2-127">-Name</span></span>
<span data-ttu-id="f21b2-128">A létrehozható társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f21b2-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="f21b2-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f21b2-129">-PeerAddressType</span></span>
<span data-ttu-id="f21b2-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f21b2-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="f21b2-131">-PeerASN</span></span>
<span data-ttu-id="f21b2-132">Az ExpressRoute-áramkör AS-száma.</span><span class="sxs-lookup"><span data-stu-id="f21b2-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="f21b2-133">Nyilvános ASN-nek kell lennie, ha a Társviszony-típus az AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="f21b2-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f21b2-134">-PeeringType</span></span>
<span data-ttu-id="f21b2-135">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f21b2-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f21b2-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="f21b2-137">Ez a társviszony elsődleges útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="f21b2-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="f21b2-138">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f21b2-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f21b2-139">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="f21b2-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f21b2-140">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="f21b2-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="f21b2-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f21b2-141">-RouteFilter</span></span>
<span data-ttu-id="f21b2-142">Ez egy meglévő RouteFilter-objektum.</span><span class="sxs-lookup"><span data-stu-id="f21b2-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="f21b2-143">-RouteFilterId</span></span>
<span data-ttu-id="f21b2-144">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f21b2-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f21b2-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="f21b2-146">Ez a társviszony másodlagos útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="f21b2-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="f21b2-147">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f21b2-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f21b2-148">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="f21b2-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f21b2-149">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="f21b2-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="f21b2-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f21b2-150">-SharedKey</span></span>
<span data-ttu-id="f21b2-151">Ez egy opcionális MD5-kivonat, amely elő megosztott kulcsként használatos a társviszony-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="f21b2-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="f21b2-152">-VlanId</span></span>
<span data-ttu-id="f21b2-153">Ez a társviszonyhoz rendelt VLAN azonosítószáma.</span><span class="sxs-lookup"><span data-stu-id="f21b2-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21b2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21b2-154">CommonParameters</span></span>
<span data-ttu-id="f21b2-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21b2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21b2-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f21b2-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21b2-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f21b2-157">INPUTS</span></span>

### <span data-ttu-id="f21b2-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f21b2-158">System.String</span></span>

### <span data-ttu-id="f21b2-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f21b2-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="f21b2-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f21b2-160">System.Boolean</span></span>

## <span data-ttu-id="f21b2-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f21b2-161">OUTPUTS</span></span>

### <span data-ttu-id="f21b2-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="f21b2-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f21b2-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f21b2-163">NOTES</span></span>

## <span data-ttu-id="f21b2-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f21b2-164">RELATED LINKS</span></span>

[<span data-ttu-id="f21b2-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f21b2-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f21b2-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f21b2-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f21b2-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f21b2-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f21b2-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f21b2-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
