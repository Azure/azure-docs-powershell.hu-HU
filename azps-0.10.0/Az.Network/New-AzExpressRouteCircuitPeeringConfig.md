---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 28983a4b39abeeeba20223f3acd31703bbfb575f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841366"
---
# <span data-ttu-id="0ab9e-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab9e-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0ab9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ab9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab9e-103">Új társközi konfiguráció létrehozása, amelyet egy ExpressRoute-áramkörhöz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0ab9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ab9e-104">SYNTAX</span></span>

### <span data-ttu-id="0ab9e-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ab9e-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ab9e-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="0ab9e-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ab9e-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="0ab9e-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab9e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ab9e-108">DESCRIPTION</span></span>
<span data-ttu-id="0ab9e-109">A **New-AzExpressRouteCircuitPeeringConfig** parancsmag egy társközi konfigurációt ad hozzá egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="0ab9e-110">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="0ab9e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0ab9e-111">EXAMPLES</span></span>

### <span data-ttu-id="0ab9e-112">Példa 1: új ExpressRoute-áramkör létrehozása egyenrangú konfigurációval</span><span class="sxs-lookup"><span data-stu-id="0ab9e-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
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

## <span data-ttu-id="0ab9e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ab9e-113">PARAMETERS</span></span>

### <span data-ttu-id="0ab9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab9e-114">-DefaultProfile</span></span>
<span data-ttu-id="0ab9e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="0ab9e-116">-LegacyMode</span></span>
<span data-ttu-id="0ab9e-117">A társas nézet örökölt üzemmódja</span><span class="sxs-lookup"><span data-stu-id="0ab9e-117">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="0ab9e-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="0ab9e-119">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="0ab9e-120">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="0ab9e-121">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="0ab9e-122">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="0ab9e-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="0ab9e-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="0ab9e-124">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="0ab9e-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="0ab9e-126">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ab9e-127">-Name</span></span>
<span data-ttu-id="0ab9e-128">A létrehozandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-128">The name of the peering configuration to be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0ab9e-129">-PeerAddressType</span></span>
<span data-ttu-id="0ab9e-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0ab9e-130">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="0ab9e-131">-PeerASN</span></span>
<span data-ttu-id="0ab9e-132">A ExpressRoute-áramkör számának.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="0ab9e-133">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0ab9e-134">-PeeringType</span></span>
<span data-ttu-id="0ab9e-135">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0ab9e-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0ab9e-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="0ab9e-137">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="0ab9e-138">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="0ab9e-139">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="0ab9e-140">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ab9e-141">-RouteFilter</span></span>
<span data-ttu-id="0ab9e-142">Ez egy meglévő RouteFilter objektum.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="0ab9e-143">-RouteFilterId</span></span>
<span data-ttu-id="0ab9e-144">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0ab9e-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="0ab9e-146">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="0ab9e-147">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="0ab9e-148">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="0ab9e-149">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="0ab9e-150">-SharedKey</span></span>
<span data-ttu-id="0ab9e-151">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="0ab9e-152">-VlanId</span></span>
<span data-ttu-id="0ab9e-153">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="0ab9e-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab9e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab9e-154">CommonParameters</span></span>
<span data-ttu-id="0ab9e-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ab9e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab9e-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab9e-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab9e-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ab9e-157">INPUTS</span></span>

## <span data-ttu-id="0ab9e-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ab9e-158">OUTPUTS</span></span>

### <span data-ttu-id="0ab9e-159">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="0ab9e-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="0ab9e-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ab9e-160">NOTES</span></span>

## <span data-ttu-id="0ab9e-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ab9e-161">RELATED LINKS</span></span>

[<span data-ttu-id="0ab9e-162">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab9e-162">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0ab9e-163">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ab9e-163">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0ab9e-164">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab9e-164">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0ab9e-165">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ab9e-165">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
