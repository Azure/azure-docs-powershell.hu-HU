---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 3a97562c775c901e8226d1dc5a0b9d090f8f70cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843649"
---
# <span data-ttu-id="8ed13-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ed13-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="8ed13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ed13-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed13-103">Menti a módosított ExpressRoute-társközi konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="8ed13-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="8ed13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ed13-104">SYNTAX</span></span>

### <span data-ttu-id="8ed13-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ed13-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ed13-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="8ed13-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ed13-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="8ed13-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ed13-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ed13-108">DESCRIPTION</span></span>
<span data-ttu-id="8ed13-109">A **set-AzExpressRouteCircuitPeeringConfig** parancsmagok egy módosított ExpressRoute-konfigurációt mentek vissza az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="8ed13-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="8ed13-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8ed13-110">EXAMPLES</span></span>

### <span data-ttu-id="8ed13-111">Példa 1: meglévő társközi konfiguráció módosítása</span><span class="sxs-lookup"><span data-stu-id="8ed13-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="8ed13-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ed13-112">PARAMETERS</span></span>

### <span data-ttu-id="8ed13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed13-113">-DefaultProfile</span></span>
<span data-ttu-id="8ed13-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ed13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ed13-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ed13-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8ed13-116">A módosítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramköri objektum.</span><span class="sxs-lookup"><span data-stu-id="8ed13-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="8ed13-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="8ed13-117">-LegacyMode</span></span>
<span data-ttu-id="8ed13-118">A társas nézet örökölt üzemmódja</span><span class="sxs-lookup"><span data-stu-id="8ed13-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="8ed13-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="8ed13-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="8ed13-120">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="8ed13-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="8ed13-121">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8ed13-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="8ed13-122">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="8ed13-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="8ed13-123">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="8ed13-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="8ed13-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="8ed13-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="8ed13-125">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="8ed13-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="8ed13-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="8ed13-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="8ed13-127">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="8ed13-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="8ed13-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ed13-128">-Name</span></span>
<span data-ttu-id="8ed13-129">A módosítani kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="8ed13-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="8ed13-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8ed13-130">-PeerAddressType</span></span>
<span data-ttu-id="8ed13-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8ed13-131">PeerAddressType</span></span>

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

### <span data-ttu-id="8ed13-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="8ed13-132">-PeerASN</span></span>
<span data-ttu-id="8ed13-133">A ExpressRoute-áramkör számának.</span><span class="sxs-lookup"><span data-stu-id="8ed13-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="8ed13-134">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8ed13-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="8ed13-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8ed13-135">-PeeringType</span></span>
<span data-ttu-id="8ed13-136">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8ed13-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8ed13-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ed13-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="8ed13-138">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="8ed13-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="8ed13-139">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="8ed13-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8ed13-140">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="8ed13-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8ed13-141">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="8ed13-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8ed13-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8ed13-142">-RouteFilter</span></span>
<span data-ttu-id="8ed13-143">Ez egy meglévő RouteFilter objektum.</span><span class="sxs-lookup"><span data-stu-id="8ed13-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="8ed13-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="8ed13-144">-RouteFilterId</span></span>
<span data-ttu-id="8ed13-145">Ez egy meglévő RouteFilter-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ed13-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="8ed13-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ed13-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="8ed13-147">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="8ed13-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="8ed13-148">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="8ed13-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8ed13-149">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="8ed13-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8ed13-150">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="8ed13-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8ed13-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8ed13-151">-SharedKey</span></span>
<span data-ttu-id="8ed13-152">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="8ed13-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="8ed13-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="8ed13-153">-VlanId</span></span>
<span data-ttu-id="8ed13-154">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="8ed13-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="8ed13-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed13-155">CommonParameters</span></span>
<span data-ttu-id="8ed13-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ed13-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed13-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ed13-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed13-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ed13-158">INPUTS</span></span>

### <span data-ttu-id="8ed13-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ed13-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="8ed13-160">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8ed13-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="8ed13-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ed13-161">OUTPUTS</span></span>

### <span data-ttu-id="8ed13-162">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ed13-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8ed13-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ed13-163">NOTES</span></span>

## <span data-ttu-id="8ed13-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ed13-164">RELATED LINKS</span></span>

[<span data-ttu-id="8ed13-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ed13-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8ed13-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ed13-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8ed13-167">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ed13-167">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8ed13-168">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ed13-168">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
