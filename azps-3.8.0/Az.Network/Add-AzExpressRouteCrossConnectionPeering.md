---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012071"
---
# <span data-ttu-id="e107e-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="e107e-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="e107e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e107e-102">SYNOPSIS</span></span>
<span data-ttu-id="e107e-103">Egy társközi konfigurációt ad hozzá egy ExpressRoute-kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="e107e-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="e107e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e107e-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e107e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e107e-105">DESCRIPTION</span></span>
<span data-ttu-id="e107e-106">Az **Add-AzExpressRouteCrossConnectionPeering** parancsmag egy társközi konfigurációt ad hozzá egy ExpressRoute-kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="e107e-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="e107e-107">Felhívjuk a figyelmét arra, hogy a **AzExpressRouteCrossConnectionPeering** futtatása után az Set-AzExpressRouteCrossConnection parancsmagot kell hívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="e107e-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="e107e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e107e-108">EXAMPLES</span></span>

### <span data-ttu-id="e107e-109">1. példa: meglévő ExpressRoute-kapcsolat hozzáadása társközi kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e107e-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="e107e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e107e-110">PARAMETERS</span></span>

### <span data-ttu-id="e107e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e107e-111">-DefaultProfile</span></span>
<span data-ttu-id="e107e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e107e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e107e-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e107e-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="e107e-114">A ExpressRoute-kereszt kapcsolata módosul.</span><span class="sxs-lookup"><span data-stu-id="e107e-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="e107e-115">Ez az Azure objektum a **Get-AzExpressRouteCrossConnection** parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="e107e-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="e107e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e107e-116">-Force</span></span>
<span data-ttu-id="e107e-117">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e107e-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e107e-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="e107e-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="e107e-119">A MicrosoftPeering PeeringType meg kell adnia azoknak az ELŐTAGOKNAK a listáját, amelyeket meg szeretne hirdetni a BGP-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="e107e-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="e107e-120">Csak a nyilvános IP-címet fogadja el a rendszer.</span><span class="sxs-lookup"><span data-stu-id="e107e-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="e107e-121">Vesszővel elválasztott listát küldhet, ha megtervezi az előtagok küldését.</span><span class="sxs-lookup"><span data-stu-id="e107e-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="e107e-122">Ezeket az előtagokat regisztrálnia kell Önnek egy útválasztási beállításjegyzék nevében (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="e107e-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="e107e-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="e107e-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="e107e-124">Ha olyan előtagokat ad meg, amelyek nem szerepelnek a megtekintő listában, megadhatja azt a számot, amelyre a számot regisztrálta.</span><span class="sxs-lookup"><span data-stu-id="e107e-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="e107e-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="e107e-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="e107e-126">Annak a művelettervnek a neve (RIR/IRR), amelyhez az AS szám és az előtagok regisztráltak.</span><span class="sxs-lookup"><span data-stu-id="e107e-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="e107e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e107e-127">-Name</span></span>
<span data-ttu-id="e107e-128">A hozzáadni kívánt társközi kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="e107e-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="e107e-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e107e-129">-PeerAddressType</span></span>
<span data-ttu-id="e107e-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e107e-130">PeerAddressType</span></span>

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

### <span data-ttu-id="e107e-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="e107e-131">-PeerASN</span></span>
<span data-ttu-id="e107e-132">Az ExpressRoute közötti kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="e107e-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="e107e-133">A PeeringType AzurePublicPeering nyilvános ASN-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e107e-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="e107e-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e107e-134">-PeeringType</span></span>
<span data-ttu-id="e107e-135">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e107e-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e107e-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e107e-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="e107e-137">Ez a kapcsolati kapcsolat elsődleges útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e107e-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="e107e-138">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="e107e-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e107e-139">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="e107e-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e107e-140">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="e107e-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e107e-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e107e-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="e107e-142">Ez a kapcsolati kapcsolat másodlagos útválasztási elérési útjának IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e107e-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="e107e-143">Ennek kell lennie a/30 CIDR alhálózatnak.</span><span class="sxs-lookup"><span data-stu-id="e107e-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e107e-144">Az alhálózatban lévő első páratlan címet az útválasztó felületéhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="e107e-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e107e-145">Az Azure a következő páros számú címet fogja konfigurálni az Azure router felületén.</span><span class="sxs-lookup"><span data-stu-id="e107e-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e107e-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e107e-146">-SharedKey</span></span>
<span data-ttu-id="e107e-147">Ez egy opcionális MD5-ujjlenyomat, amelyet előre megosztott kulcsként használ a társközi konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="e107e-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="e107e-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="e107e-148">-VlanId</span></span>
<span data-ttu-id="e107e-149">Ez a munkatárshoz hozzárendelt VLAN azonosító száma.</span><span class="sxs-lookup"><span data-stu-id="e107e-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="e107e-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e107e-150">-Confirm</span></span>
<span data-ttu-id="e107e-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e107e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e107e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e107e-152">-WhatIf</span></span>
<span data-ttu-id="e107e-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e107e-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e107e-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e107e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e107e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e107e-155">CommonParameters</span></span>
<span data-ttu-id="e107e-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e107e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e107e-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e107e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e107e-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e107e-158">INPUTS</span></span>

### <span data-ttu-id="e107e-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e107e-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="e107e-160">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e107e-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="e107e-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e107e-161">OUTPUTS</span></span>

### <span data-ttu-id="e107e-162">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e107e-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="e107e-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e107e-163">NOTES</span></span>

## <span data-ttu-id="e107e-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e107e-164">RELATED LINKS</span></span>

[<span data-ttu-id="e107e-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="e107e-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="e107e-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="e107e-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="e107e-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e107e-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="e107e-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e107e-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
