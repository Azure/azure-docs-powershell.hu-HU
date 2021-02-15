---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151435"
---
# <span data-ttu-id="57f9e-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f9e-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="57f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="57f9e-103">Módosított ExpressRoute-társviszony-konfigurációt ment.</span><span class="sxs-lookup"><span data-stu-id="57f9e-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="57f9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57f9e-104">SYNTAX</span></span>

### <span data-ttu-id="57f9e-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57f9e-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57f9e-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="57f9e-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57f9e-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="57f9e-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f9e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57f9e-108">DESCRIPTION</span></span>
<span data-ttu-id="57f9e-109">A **Set-AzExpressRouteCircuitPeeringConfig** parancsmagok a módosított ExpressRoute-társviszony-konfigurációt az Azure-ba mentik.</span><span class="sxs-lookup"><span data-stu-id="57f9e-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="57f9e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57f9e-110">EXAMPLES</span></span>

### <span data-ttu-id="57f9e-111">1. példa: Meglévő társviszony-konfiguráció módosítása</span><span class="sxs-lookup"><span data-stu-id="57f9e-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="57f9e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="57f9e-112">Example 2</span></span>

<span data-ttu-id="57f9e-113">Módosított ExpressRoute-társviszony-konfigurációt ment.</span><span class="sxs-lookup"><span data-stu-id="57f9e-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="57f9e-114">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="57f9e-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="57f9e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57f9e-115">PARAMETERS</span></span>

### <span data-ttu-id="57f9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f9e-116">-DefaultProfile</span></span>
<span data-ttu-id="57f9e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57f9e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57f9e-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f9e-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="57f9e-119">A módosítható társviszony-konfigurációt tartalmazó ExpressRoute-áramkör-objektum.</span><span class="sxs-lookup"><span data-stu-id="57f9e-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="57f9e-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="57f9e-120">-LegacyMode</span></span>
<span data-ttu-id="57f9e-121">A társviszony-létesítés régi módja</span><span class="sxs-lookup"><span data-stu-id="57f9e-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="57f9e-122">-MicrosoftConfigAdvertedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="57f9e-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="57f9e-123">A MicrosoftPeering társviszony-típusa esetében meg kell adnia a BGP-munkameneten keresztül meghirdetett összes előtag listáját.</span><span class="sxs-lookup"><span data-stu-id="57f9e-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="57f9e-124">Csak a nyilvános IP-cím előtagokat fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="57f9e-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="57f9e-125">Vesszővel elválasztott listát is küldhet, ha előtagokat tervez küldeni.</span><span class="sxs-lookup"><span data-stu-id="57f9e-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="57f9e-126">Ezeket az előtagokat a Routing Registry Name (RIR/IRR) névben kell regisztrálnia.</span><span class="sxs-lookup"><span data-stu-id="57f9e-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="57f9e-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="57f9e-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="57f9e-128">Ha Ön olyan hirdetési előtagokat ad meg, amelyek nem a társviszony-létesítő AS számhoz vannak regisztrálva, megadhatja azt az AS-számot, amelyre regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="57f9e-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="57f9e-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="57f9e-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="57f9e-130">Az Routing Registry Name (RIR/BRR), amelyre az AS szám és az előtagok regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="57f9e-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="57f9e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="57f9e-131">-Name</span></span>
<span data-ttu-id="57f9e-132">A módosítható társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="57f9e-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="57f9e-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="57f9e-133">-PeerAddressType</span></span>
<span data-ttu-id="57f9e-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="57f9e-134">PeerAddressType</span></span>

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

### <span data-ttu-id="57f9e-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="57f9e-135">-PeerASN</span></span>
<span data-ttu-id="57f9e-136">Az ExpressRoute-áramkör AS-száma.</span><span class="sxs-lookup"><span data-stu-id="57f9e-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="57f9e-137">Nyilvános ASN-nek kell lennie, ha a Társviszony-típus az AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="57f9e-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="57f9e-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="57f9e-138">-PeeringType</span></span>
<span data-ttu-id="57f9e-139">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="57f9e-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="57f9e-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57f9e-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="57f9e-141">Ez a társviszony elsődleges útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="57f9e-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="57f9e-142">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="57f9e-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="57f9e-143">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="57f9e-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="57f9e-144">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="57f9e-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="57f9e-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="57f9e-145">-RouteFilter</span></span>
<span data-ttu-id="57f9e-146">Ez egy meglévő RouteFilter-objektum.</span><span class="sxs-lookup"><span data-stu-id="57f9e-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="57f9e-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="57f9e-147">-RouteFilterId</span></span>
<span data-ttu-id="57f9e-148">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57f9e-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="57f9e-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57f9e-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="57f9e-150">Ez a társviszony másodlagos útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="57f9e-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="57f9e-151">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="57f9e-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="57f9e-152">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="57f9e-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="57f9e-153">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="57f9e-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="57f9e-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="57f9e-154">-SharedKey</span></span>
<span data-ttu-id="57f9e-155">Ez egy opcionális MD5-kivonat, amely elő megosztott kulcsként használatos a társviszony-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="57f9e-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="57f9e-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="57f9e-156">-VlanId</span></span>
<span data-ttu-id="57f9e-157">Ez a társviszonyhoz rendelt VLAN azonosítószáma.</span><span class="sxs-lookup"><span data-stu-id="57f9e-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="57f9e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f9e-158">CommonParameters</span></span>
<span data-ttu-id="57f9e-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f9e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f9e-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f9e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f9e-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57f9e-161">INPUTS</span></span>

### <span data-ttu-id="57f9e-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f9e-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="57f9e-163">System.String</span><span class="sxs-lookup"><span data-stu-id="57f9e-163">System.String</span></span>

### <span data-ttu-id="57f9e-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="57f9e-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="57f9e-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57f9e-165">System.Boolean</span></span>

## <span data-ttu-id="57f9e-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57f9e-166">OUTPUTS</span></span>

### <span data-ttu-id="57f9e-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f9e-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="57f9e-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57f9e-168">NOTES</span></span>

## <span data-ttu-id="57f9e-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57f9e-169">RELATED LINKS</span></span>

[<span data-ttu-id="57f9e-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f9e-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="57f9e-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f9e-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="57f9e-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f9e-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="57f9e-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f9e-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
