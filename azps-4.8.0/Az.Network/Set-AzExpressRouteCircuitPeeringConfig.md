---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184325"
---
# <span data-ttu-id="575ed-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="575ed-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="575ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="575ed-102">SYNOPSIS</span></span>
<span data-ttu-id="575ed-103">Menti a módosított ExpressRoute-társközi konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="575ed-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="575ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="575ed-104">SYNTAX</span></span>

### <span data-ttu-id="575ed-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="575ed-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="575ed-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="575ed-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="575ed-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="575ed-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="575ed-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="575ed-108">DESCRIPTION</span></span>
<span data-ttu-id="575ed-109">A **set-AzExpressRouteCircuitPeeringConfig** parancsmagok egy módosított ExpressRoute-konfigurációt mentek vissza az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="575ed-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="575ed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="575ed-110">EXAMPLES</span></span>

### <span data-ttu-id="575ed-111">Példa 1: meglévő társközi konfiguráció módosítása</span><span class="sxs-lookup"><span data-stu-id="575ed-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="575ed-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="575ed-112">Example 2</span></span>

<span data-ttu-id="575ed-113">Menti a módosított ExpressRoute-társközi konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="575ed-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="575ed-114">autogenerated</span><span class="sxs-lookup"><span data-stu-id="575ed-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="575ed-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="575ed-115">PARAMETERS</span></span>

### <span data-ttu-id="575ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575ed-116">-DefaultProfile</span></span>
<span data-ttu-id="575ed-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="575ed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="575ed-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="575ed-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="575ed-119">A módosítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramköri objektum.</span><span class="sxs-lookup"><span data-stu-id="575ed-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="575ed-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="575ed-120">-LegacyMode</span></span>
<span data-ttu-id="575ed-121">A társas nézet örökölt üzemmódja</span><span class="sxs-lookup"><span data-stu-id="575ed-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="575ed-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="575ed-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="575ed-123">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="575ed-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="575ed-124">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="575ed-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="575ed-125">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="575ed-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="575ed-126">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="575ed-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="575ed-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="575ed-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="575ed-128">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="575ed-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="575ed-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="575ed-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="575ed-130">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="575ed-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="575ed-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="575ed-131">-Name</span></span>
<span data-ttu-id="575ed-132">A módosítani kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="575ed-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="575ed-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="575ed-133">-PeerAddressType</span></span>
<span data-ttu-id="575ed-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="575ed-134">PeerAddressType</span></span>

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

### <span data-ttu-id="575ed-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="575ed-135">-PeerASN</span></span>
<span data-ttu-id="575ed-136">A ExpressRoute-áramkör számának.</span><span class="sxs-lookup"><span data-stu-id="575ed-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="575ed-137">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="575ed-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="575ed-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="575ed-138">-PeeringType</span></span>
<span data-ttu-id="575ed-139">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="575ed-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="575ed-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="575ed-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="575ed-141">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="575ed-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="575ed-142">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="575ed-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="575ed-143">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="575ed-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="575ed-144">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="575ed-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="575ed-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="575ed-145">-RouteFilter</span></span>
<span data-ttu-id="575ed-146">Ez egy meglévő RouteFilter objektum.</span><span class="sxs-lookup"><span data-stu-id="575ed-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="575ed-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="575ed-147">-RouteFilterId</span></span>
<span data-ttu-id="575ed-148">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="575ed-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="575ed-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="575ed-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="575ed-150">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="575ed-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="575ed-151">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="575ed-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="575ed-152">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="575ed-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="575ed-153">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="575ed-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="575ed-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="575ed-154">-SharedKey</span></span>
<span data-ttu-id="575ed-155">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="575ed-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="575ed-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="575ed-156">-VlanId</span></span>
<span data-ttu-id="575ed-157">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="575ed-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="575ed-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575ed-158">CommonParameters</span></span>
<span data-ttu-id="575ed-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="575ed-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575ed-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575ed-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575ed-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="575ed-161">INPUTS</span></span>

### <span data-ttu-id="575ed-162">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="575ed-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="575ed-163">System. String</span><span class="sxs-lookup"><span data-stu-id="575ed-163">System.String</span></span>

### <span data-ttu-id="575ed-164">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="575ed-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="575ed-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="575ed-165">System.Boolean</span></span>

## <span data-ttu-id="575ed-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="575ed-166">OUTPUTS</span></span>

### <span data-ttu-id="575ed-167">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="575ed-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="575ed-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="575ed-168">NOTES</span></span>

## <span data-ttu-id="575ed-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="575ed-169">RELATED LINKS</span></span>

[<span data-ttu-id="575ed-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="575ed-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="575ed-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="575ed-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="575ed-172">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="575ed-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="575ed-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="575ed-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
