---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187248"
---
# <span data-ttu-id="7d4a5-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d4a5-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="7d4a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4a5-103">Menti a módosított ExpressRoute-társközi konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="7d4a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d4a5-104">SYNTAX</span></span>

### <span data-ttu-id="7d4a5-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d4a5-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4a5-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="7d4a5-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4a5-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="7d4a5-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4a5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d4a5-108">DESCRIPTION</span></span>
<span data-ttu-id="7d4a5-109">A **set-AzExpressRouteCircuitPeeringConfig** parancsmagok egy módosított ExpressRoute-konfigurációt mentek vissza az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="7d4a5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7d4a5-110">EXAMPLES</span></span>

### <span data-ttu-id="7d4a5-111">Példa 1: meglévő társközi konfiguráció módosítása</span><span class="sxs-lookup"><span data-stu-id="7d4a5-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="7d4a5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7d4a5-112">Example 2</span></span>

<span data-ttu-id="7d4a5-113">Menti a módosított ExpressRoute-társközi konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="7d4a5-114">autogenerated</span><span class="sxs-lookup"><span data-stu-id="7d4a5-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="7d4a5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d4a5-115">PARAMETERS</span></span>

### <span data-ttu-id="7d4a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4a5-116">-DefaultProfile</span></span>
<span data-ttu-id="7d4a5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d4a5-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d4a5-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7d4a5-119">A módosítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramköri objektum.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="7d4a5-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="7d4a5-120">-LegacyMode</span></span>
<span data-ttu-id="7d4a5-121">A társas nézet örökölt üzemmódja</span><span class="sxs-lookup"><span data-stu-id="7d4a5-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="7d4a5-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="7d4a5-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="7d4a5-123">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="7d4a5-124">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="7d4a5-125">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="7d4a5-126">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="7d4a5-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="7d4a5-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="7d4a5-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="7d4a5-128">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="7d4a5-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="7d4a5-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="7d4a5-130">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="7d4a5-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d4a5-131">-Name</span></span>
<span data-ttu-id="7d4a5-132">A módosítani kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="7d4a5-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7d4a5-133">-PeerAddressType</span></span>
<span data-ttu-id="7d4a5-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7d4a5-134">PeerAddressType</span></span>

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

### <span data-ttu-id="7d4a5-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="7d4a5-135">-PeerASN</span></span>
<span data-ttu-id="7d4a5-136">A ExpressRoute-áramkör számának.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="7d4a5-137">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="7d4a5-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7d4a5-138">-PeeringType</span></span>
<span data-ttu-id="7d4a5-139">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7d4a5-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7d4a5-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d4a5-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="7d4a5-141">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="7d4a5-142">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7d4a5-143">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7d4a5-144">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7d4a5-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d4a5-145">-RouteFilter</span></span>
<span data-ttu-id="7d4a5-146">Ez egy meglévő RouteFilter objektum.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="7d4a5-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="7d4a5-147">-RouteFilterId</span></span>
<span data-ttu-id="7d4a5-148">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="7d4a5-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d4a5-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="7d4a5-150">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="7d4a5-151">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7d4a5-152">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7d4a5-153">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7d4a5-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7d4a5-154">-SharedKey</span></span>
<span data-ttu-id="7d4a5-155">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="7d4a5-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="7d4a5-156">-VlanId</span></span>
<span data-ttu-id="7d4a5-157">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="7d4a5-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="7d4a5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4a5-158">CommonParameters</span></span>
<span data-ttu-id="7d4a5-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d4a5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4a5-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4a5-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4a5-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d4a5-161">INPUTS</span></span>

### <span data-ttu-id="7d4a5-162">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d4a5-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="7d4a5-163">System. String</span><span class="sxs-lookup"><span data-stu-id="7d4a5-163">System.String</span></span>

### <span data-ttu-id="7d4a5-164">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d4a5-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="7d4a5-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d4a5-165">System.Boolean</span></span>

## <span data-ttu-id="7d4a5-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d4a5-166">OUTPUTS</span></span>

### <span data-ttu-id="7d4a5-167">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d4a5-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7d4a5-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d4a5-168">NOTES</span></span>

## <span data-ttu-id="7d4a5-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d4a5-169">RELATED LINKS</span></span>

[<span data-ttu-id="7d4a5-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d4a5-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d4a5-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d4a5-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7d4a5-172">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d4a5-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d4a5-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d4a5-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
