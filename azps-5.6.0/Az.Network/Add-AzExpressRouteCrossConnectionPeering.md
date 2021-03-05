---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011910"
---
# <span data-ttu-id="7710a-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7710a-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="7710a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7710a-102">SYNOPSIS</span></span>
<span data-ttu-id="7710a-103">Társviszony-konfigurációt ad egy ExpressRoute-kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="7710a-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7710a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7710a-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7710a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7710a-105">DESCRIPTION</span></span>
<span data-ttu-id="7710a-106">Az **Add-AzExpressRouteCrossConnectionPeering** parancsmag társviszony-konfigurációt ad az ExpressRoute-kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="7710a-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="7710a-107">Vegye figyelembe, hogy az **Add-AzExpressRouteCrossConnectionPeering** futtatása után a Set-AzExpressRouteCrossConnection parancsmagot kell felhívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="7710a-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="7710a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7710a-108">EXAMPLES</span></span>

### <span data-ttu-id="7710a-109">1. példa: Társ felvétele meglévő ExpressRoute-keresztkapcsolatba</span><span class="sxs-lookup"><span data-stu-id="7710a-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="7710a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7710a-110">PARAMETERS</span></span>

### <span data-ttu-id="7710a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7710a-111">-DefaultProfile</span></span>
<span data-ttu-id="7710a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7710a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7710a-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7710a-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7710a-114">Az ExpressRoute-kapcsolat módosítása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="7710a-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="7710a-115">Ez a **Get-AzExpressRouteCrossConnection** parancsmag által visszaadott Azure-objektum.</span><span class="sxs-lookup"><span data-stu-id="7710a-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7710a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7710a-116">-Force</span></span>
<span data-ttu-id="7710a-117">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="7710a-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7710a-118">-MicrosoftConfigAdvertedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="7710a-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="7710a-119">A MicrosoftPeering társviszony-típusa esetében meg kell adnia a BGP-munkameneten keresztül meghirdetni tervezhető előtagok listáját.</span><span class="sxs-lookup"><span data-stu-id="7710a-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="7710a-120">Csak a nyilvános IP-cím előtagokat fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7710a-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="7710a-121">Vesszővel elválasztott listát is küldhet, ha előtagokat tervez küldeni.</span><span class="sxs-lookup"><span data-stu-id="7710a-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="7710a-122">Ezeket az előtagokat a Routing Registry Name (RIR/IRR) névben kell regisztrálnia.</span><span class="sxs-lookup"><span data-stu-id="7710a-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="7710a-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="7710a-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="7710a-124">Ha Ön olyan hirdetési előtagokat ad meg, amelyek nem a társviszony-létesítő AS számhoz vannak regisztrálva, megadhatja azt az AS-számot, amelyre regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="7710a-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="7710a-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="7710a-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="7710a-126">A routing registry name (RIR /BRR), amelyre az AS szám és az előtagok regisztrálva vannak.</span><span class="sxs-lookup"><span data-stu-id="7710a-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="7710a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7710a-127">-Name</span></span>
<span data-ttu-id="7710a-128">A hozzáadható társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="7710a-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="7710a-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7710a-129">-PeerAddressType</span></span>
<span data-ttu-id="7710a-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7710a-130">PeerAddressType</span></span>

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

### <span data-ttu-id="7710a-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="7710a-131">-PeerASN</span></span>
<span data-ttu-id="7710a-132">Az ExpressRoute-keresztkapcsolat AS-száma.</span><span class="sxs-lookup"><span data-stu-id="7710a-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="7710a-133">Nyilvános ASN-nek kell lennie, ha a Társviszony-típus az AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="7710a-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="7710a-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7710a-134">-PeeringType</span></span>
<span data-ttu-id="7710a-135">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7710a-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7710a-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7710a-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="7710a-137">Ez a társviszony elsődleges útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="7710a-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="7710a-138">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7710a-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7710a-139">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="7710a-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7710a-140">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="7710a-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7710a-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7710a-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="7710a-142">Ez a társviszony másodlagos útválasztási útvonalának IP-címtartománya.</span><span class="sxs-lookup"><span data-stu-id="7710a-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="7710a-143">Ennek egy /30 CIDR alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7710a-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7710a-144">Az alhálózat első páratlan címét hozzá kell rendelni az útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="7710a-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7710a-145">Az Azure beállítja a következő, egyenletesen számmal megadott címet az Azure útválasztó felületéhez.</span><span class="sxs-lookup"><span data-stu-id="7710a-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7710a-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7710a-146">-SharedKey</span></span>
<span data-ttu-id="7710a-147">Ez egy opcionális MD5-kivonat, amely elő megosztott kulcsként használatos a társviszony-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="7710a-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="7710a-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="7710a-148">-VlanId</span></span>
<span data-ttu-id="7710a-149">Ez a társviszonyhoz rendelt VLAN azonosítószáma.</span><span class="sxs-lookup"><span data-stu-id="7710a-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="7710a-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7710a-150">-Confirm</span></span>
<span data-ttu-id="7710a-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7710a-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7710a-152">-WhatIf</span></span>
<span data-ttu-id="7710a-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7710a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7710a-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7710a-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7710a-155">CommonParameters</span></span>
<span data-ttu-id="7710a-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7710a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7710a-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7710a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7710a-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7710a-158">INPUTS</span></span>

### <span data-ttu-id="7710a-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7710a-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="7710a-160">Az "ExpressRouteCrossConnection" paraméter a "PSExpressRouteCrossConnection" típusú értéket fogadja el a folyamatból.</span><span class="sxs-lookup"><span data-stu-id="7710a-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="7710a-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7710a-161">OUTPUTS</span></span>

### <span data-ttu-id="7710a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7710a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7710a-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7710a-163">NOTES</span></span>

## <span data-ttu-id="7710a-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7710a-164">RELATED LINKS</span></span>

[<span data-ttu-id="7710a-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7710a-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7710a-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7710a-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7710a-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7710a-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="7710a-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7710a-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
