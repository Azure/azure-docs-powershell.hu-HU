---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480012"
---
# <span data-ttu-id="3da22-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3da22-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="3da22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3da22-102">SYNOPSIS</span></span>
<span data-ttu-id="3da22-103">Társviszony-konfigurációt ad egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="3da22-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="3da22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3da22-104">SYNTAX</span></span>

### <span data-ttu-id="3da22-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3da22-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3da22-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="3da22-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3da22-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="3da22-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3da22-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3da22-108">DESCRIPTION</span></span>
<span data-ttu-id="3da22-109">Az **Add-AzExpressRouteCircuitPeeringConfig** parancsmag társviszony-konfigurációt ad egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="3da22-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="3da22-110">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz.</span><span class="sxs-lookup"><span data-stu-id="3da22-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3da22-111">Vegye figyelembe, hogy az **Add-AzExpressRouteCircuitPeeringConfig** futtatása után a Set-AzExpressRouteCircuit parancsmagot kell felhívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="3da22-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="3da22-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3da22-112">EXAMPLES</span></span>

### <span data-ttu-id="3da22-113">1. példa: Társ hozzáadása meglévő ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="3da22-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="3da22-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3da22-114">PARAMETERS</span></span>

### <span data-ttu-id="3da22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da22-115">-DefaultProfile</span></span>
<span data-ttu-id="3da22-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3da22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da22-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3da22-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3da22-118">Az ExpressRoute-áramkör módosul.</span><span class="sxs-lookup"><span data-stu-id="3da22-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3da22-119">Ez a **Get-AzExpressRouteCircuit** parancsmag által visszaadott Azure-objektum.</span><span class="sxs-lookup"><span data-stu-id="3da22-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3da22-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="3da22-120">-LegacyMode</span></span>
<span data-ttu-id="3da22-121">A társviszony-létesítés régi módja</span><span class="sxs-lookup"><span data-stu-id="3da22-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="3da22-122">-MicrosoftConfigAdvertedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="3da22-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="3da22-123">A MicrosoftPeering társviszony-típusa esetében meg kell adnia a BGP-munkameneten keresztül meghirdetni tervezhető előtagok listáját.</span><span class="sxs-lookup"><span data-stu-id="3da22-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="3da22-124">Csak a nyilvános IP-cím előtagokat fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="3da22-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="3da22-125">Vesszővel elválasztott listát is küldhet, ha előtagokat tervez küldeni.</span><span class="sxs-lookup"><span data-stu-id="3da22-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="3da22-126">Ezeket az előtagokat a Routing Registry Name (RIR/IRR) névben kell regisztrálnia.</span><span class="sxs-lookup"><span data-stu-id="3da22-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="3da22-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="3da22-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="3da22-128">Ha Ön olyan hirdetési előtagokat ad meg, amelyek nem a társviszony-létesítő AS számhoz vannak regisztrálva, megadhatja azt az AS-számot, amelyre regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="3da22-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="3da22-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="3da22-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="3da22-130">A routing registry name (RIR /BRR), amelyre az AS szám és az előtagok regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="3da22-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="3da22-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3da22-131">-Name</span></span>
<span data-ttu-id="3da22-132">A hozzáadható társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="3da22-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="3da22-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3da22-133">-PeerAddressType</span></span>
<span data-ttu-id="3da22-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3da22-134">PeerAddressType</span></span>

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

### <span data-ttu-id="3da22-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="3da22-135">-PeerASN</span></span>
<span data-ttu-id="3da22-136">Az ExpressRoute-áramkör AS-száma.</span><span class="sxs-lookup"><span data-stu-id="3da22-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="3da22-137">Nyilvános ASN-nek kell lennie, ha a Társviszony-típus az AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="3da22-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="3da22-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3da22-138">-PeeringType</span></span>
<span data-ttu-id="3da22-139">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3da22-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3da22-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3da22-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="3da22-141">Ez a társviszony elsődleges útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="3da22-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="3da22-142">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3da22-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3da22-143">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="3da22-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3da22-144">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="3da22-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3da22-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3da22-145">-RouteFilter</span></span>
<span data-ttu-id="3da22-146">Ez egy meglévő RouteFilter-objektum.</span><span class="sxs-lookup"><span data-stu-id="3da22-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="3da22-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="3da22-147">-RouteFilterId</span></span>
<span data-ttu-id="3da22-148">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3da22-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="3da22-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3da22-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="3da22-150">Ez a társviszony másodlagos útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="3da22-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="3da22-151">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3da22-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3da22-152">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="3da22-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3da22-153">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="3da22-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3da22-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3da22-154">-SharedKey</span></span>
<span data-ttu-id="3da22-155">Ez egy opcionális MD5-kivonat, amely elő megosztott kulcsként használatos a társviszony-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="3da22-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="3da22-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="3da22-156">-VlanId</span></span>
<span data-ttu-id="3da22-157">Ez a társviszonyhoz rendelt VLAN azonosítószáma.</span><span class="sxs-lookup"><span data-stu-id="3da22-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="3da22-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da22-158">CommonParameters</span></span>
<span data-ttu-id="3da22-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da22-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da22-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da22-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da22-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3da22-161">INPUTS</span></span>

### <span data-ttu-id="3da22-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3da22-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="3da22-163">System.String</span><span class="sxs-lookup"><span data-stu-id="3da22-163">System.String</span></span>

### <span data-ttu-id="3da22-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3da22-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="3da22-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3da22-165">System.Boolean</span></span>

## <span data-ttu-id="3da22-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3da22-166">OUTPUTS</span></span>

### <span data-ttu-id="3da22-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3da22-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3da22-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3da22-168">NOTES</span></span>

## <span data-ttu-id="3da22-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3da22-169">RELATED LINKS</span></span>

[<span data-ttu-id="3da22-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3da22-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3da22-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3da22-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3da22-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3da22-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3da22-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3da22-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
