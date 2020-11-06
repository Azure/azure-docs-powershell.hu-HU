---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: aef46264bc13b7136f9f999b2a97b3dd0951fbe8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496455"
---
# <span data-ttu-id="21965-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="21965-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="21965-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21965-102">SYNOPSIS</span></span>
<span data-ttu-id="21965-103">Egy ExpressRoute-áramkörrel egyenrangú konfigurációt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="21965-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21965-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21965-104">SYNTAX</span></span>

### <span data-ttu-id="21965-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21965-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21965-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="21965-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21965-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="21965-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21965-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21965-108">DESCRIPTION</span></span>
<span data-ttu-id="21965-109">Az **Add-AzureRmExpressRouteCircuitPeeringConfig** parancsmag egy társközi konfigurációt ad hozzá egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="21965-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="21965-110">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="21965-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="21965-111">Felhívjuk a figyelmét arra, hogy a **AzureRmExpressRouteCircuitPeeringConfig** futtatása után az Set-AzureRmExpressRouteCircuit parancsmagot kell hívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="21965-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="21965-112">Példák</span><span class="sxs-lookup"><span data-stu-id="21965-112">EXAMPLES</span></span>

### <span data-ttu-id="21965-113">1. példa: társközi hozzáadása meglévő ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="21965-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="21965-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21965-114">PARAMETERS</span></span>

### <span data-ttu-id="21965-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21965-115">-DefaultProfile</span></span>
<span data-ttu-id="21965-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21965-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21965-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21965-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="21965-118">A ExpressRoute-áramkör módosul.</span><span class="sxs-lookup"><span data-stu-id="21965-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="21965-119">Ez az Azure objektum a **Get-AzureRmExpressRouteCircuit** parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="21965-119">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21965-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="21965-120">-LegacyMode</span></span>
<span data-ttu-id="21965-121">A társas nézet örökölt üzemmódja</span><span class="sxs-lookup"><span data-stu-id="21965-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="21965-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="21965-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="21965-123">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="21965-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="21965-124">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="21965-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="21965-125">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="21965-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="21965-126">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="21965-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="21965-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="21965-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="21965-128">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="21965-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="21965-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="21965-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="21965-130">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="21965-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="21965-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21965-131">-Name</span></span>
<span data-ttu-id="21965-132">A hozzáadni kívánt társközi kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="21965-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="21965-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="21965-133">-PeerAddressType</span></span>
<span data-ttu-id="21965-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="21965-134">PeerAddressType</span></span>

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

### <span data-ttu-id="21965-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="21965-135">-PeerASN</span></span>
<span data-ttu-id="21965-136">A ExpressRoute-áramkör számának.</span><span class="sxs-lookup"><span data-stu-id="21965-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="21965-137">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="21965-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21965-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="21965-138">-PeeringType</span></span>
<span data-ttu-id="21965-139">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="21965-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="21965-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="21965-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="21965-141">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="21965-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="21965-142">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="21965-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="21965-143">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="21965-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="21965-144">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="21965-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="21965-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="21965-145">-RouteFilter</span></span>
<span data-ttu-id="21965-146">Ez egy meglévő RouteFilter objektum.</span><span class="sxs-lookup"><span data-stu-id="21965-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="21965-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="21965-147">-RouteFilterId</span></span>
<span data-ttu-id="21965-148">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="21965-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="21965-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="21965-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="21965-150">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="21965-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="21965-151">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="21965-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="21965-152">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="21965-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="21965-153">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="21965-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="21965-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="21965-154">-SharedKey</span></span>
<span data-ttu-id="21965-155">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="21965-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="21965-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="21965-156">-VlanId</span></span>
<span data-ttu-id="21965-157">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="21965-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="21965-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21965-158">CommonParameters</span></span>
<span data-ttu-id="21965-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21965-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21965-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21965-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21965-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21965-161">INPUTS</span></span>

### <span data-ttu-id="21965-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21965-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="21965-163">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="21965-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="21965-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21965-164">OUTPUTS</span></span>

### <span data-ttu-id="21965-165">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21965-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="21965-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21965-166">NOTES</span></span>

## <span data-ttu-id="21965-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21965-167">RELATED LINKS</span></span>

[<span data-ttu-id="21965-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21965-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="21965-169">Új – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="21965-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="21965-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="21965-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="21965-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21965-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
