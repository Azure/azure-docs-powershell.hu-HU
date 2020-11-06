---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: f9d2cc0959cd14e76500f2da85a23c93358c7e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494458"
---
# <span data-ttu-id="7d603-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d603-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="7d603-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d603-102">SYNOPSIS</span></span>
<span data-ttu-id="7d603-103">Menti a módosított ExpressRoute-társközi konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7d603-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d603-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d603-104">SYNTAX</span></span>

### <span data-ttu-id="7d603-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d603-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d603-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="7d603-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d603-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="7d603-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d603-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d603-108">DESCRIPTION</span></span>
<span data-ttu-id="7d603-109">A **set-AzureRmExpressRouteCircuitPeeringConfig** parancsmagok egy módosított ExpressRoute-konfigurációt mentek vissza az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="7d603-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="7d603-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7d603-110">EXAMPLES</span></span>

### <span data-ttu-id="7d603-111">Példa 1: meglévő társközi konfiguráció módosítása</span><span class="sxs-lookup"><span data-stu-id="7d603-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="7d603-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d603-112">PARAMETERS</span></span>

### <span data-ttu-id="7d603-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d603-113">-DefaultProfile</span></span>
<span data-ttu-id="7d603-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d603-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d603-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d603-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7d603-116">A módosítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramköri objektum.</span><span class="sxs-lookup"><span data-stu-id="7d603-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="7d603-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="7d603-117">-LegacyMode</span></span>
<span data-ttu-id="7d603-118">A társas nézet örökölt üzemmódja</span><span class="sxs-lookup"><span data-stu-id="7d603-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="7d603-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="7d603-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="7d603-120">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="7d603-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="7d603-121">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7d603-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="7d603-122">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="7d603-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="7d603-123">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="7d603-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="7d603-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="7d603-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="7d603-125">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="7d603-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="7d603-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="7d603-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="7d603-127">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="7d603-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="7d603-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d603-128">-Name</span></span>
<span data-ttu-id="7d603-129">A módosítani kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7d603-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="7d603-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7d603-130">-PeerAddressType</span></span>
<span data-ttu-id="7d603-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7d603-131">PeerAddressType</span></span>

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

### <span data-ttu-id="7d603-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="7d603-132">-PeerASN</span></span>
<span data-ttu-id="7d603-133">A ExpressRoute-áramkör számának.</span><span class="sxs-lookup"><span data-stu-id="7d603-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="7d603-134">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7d603-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="7d603-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7d603-135">-PeeringType</span></span>
<span data-ttu-id="7d603-136">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7d603-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7d603-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d603-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="7d603-138">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="7d603-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="7d603-139">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="7d603-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7d603-140">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="7d603-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7d603-141">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="7d603-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7d603-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d603-142">-RouteFilter</span></span>
<span data-ttu-id="7d603-143">Ez egy meglévő RouteFilter objektum.</span><span class="sxs-lookup"><span data-stu-id="7d603-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="7d603-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="7d603-144">-RouteFilterId</span></span>
<span data-ttu-id="7d603-145">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d603-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="7d603-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d603-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="7d603-147">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="7d603-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="7d603-148">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="7d603-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7d603-149">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="7d603-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7d603-150">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="7d603-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7d603-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7d603-151">-SharedKey</span></span>
<span data-ttu-id="7d603-152">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="7d603-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="7d603-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="7d603-153">-VlanId</span></span>
<span data-ttu-id="7d603-154">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="7d603-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="7d603-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d603-155">CommonParameters</span></span>
<span data-ttu-id="7d603-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d603-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d603-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d603-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d603-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d603-158">INPUTS</span></span>

### <span data-ttu-id="7d603-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d603-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="7d603-160">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7d603-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="7d603-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d603-161">OUTPUTS</span></span>

### <span data-ttu-id="7d603-162">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d603-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7d603-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d603-163">NOTES</span></span>

## <span data-ttu-id="7d603-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d603-164">RELATED LINKS</span></span>

[<span data-ttu-id="7d603-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d603-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d603-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d603-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7d603-167">Új – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d603-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d603-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d603-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)
