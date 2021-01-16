---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325901"
---
# <span data-ttu-id="4bbe3-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bbe3-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="4bbe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbe3-103">Frissíti az Express Route Circuit magánjellegű társviszonyokkal létrehozott kapcsolati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="4bbe3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4bbe3-104">SYNTAX</span></span>

### <span data-ttu-id="4bbe3-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bbe3-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bbe3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbe3-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bbe3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4bbe3-107">DESCRIPTION</span></span>
<span data-ttu-id="4bbe3-108">A **Set-AzExpressRouteCircuitConnectionConfig** parancsmag frissíti az ExpressRoute-áramkörök privát társviszonyban létrehozott kapcsolati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="4bbe3-109">Ez lehetővé teszi két Express Route Circuits régiók vagy előfizetések közötti társviszony-létesítését.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="4bbe3-110">Vegye figyelembe, hogy a **Set-AzExpressRouteCircuitConnectionConfig** futtatása előtt az **Add-AzExpressRouteCircuitConnectionConfig** használatával kell hozzáadnia az áramköri kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="4bbe3-111">Ezenkívül a **Set-AzExpressRouteCircuitPeeringConfig** futtatása után a Set-AzExpressRouteCircuit parancsmagot kell felhívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="4bbe3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4bbe3-112">EXAMPLES</span></span>

### <span data-ttu-id="4bbe3-113">1. példa: Kapcsolatcsoport kapcsolati erőforrásának frissítése meglévő ExpressRoute-áramkörre</span><span class="sxs-lookup"><span data-stu-id="4bbe3-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="4bbe3-114">2. példa: Kapcsolati kapcsolat beállítása a Piping használatával egy meglévő ExpressRoute-áramkörre</span><span class="sxs-lookup"><span data-stu-id="4bbe3-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="4bbe3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bbe3-115">PARAMETERS</span></span>

### <span data-ttu-id="4bbe3-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bbe3-116">-AddressPrefix</span></span>
<span data-ttu-id="4bbe3-117">Legalább /29 ügyfélcímterület VxLan-alagutak létrehozásához az Express Route Circuits for IPv4-átjárók között.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="4bbe3-118">vagy legalább /125 ügyfélcímterületet, ahol VxLan-alagutak hozhatók létre az IPv6-alapú alagutas Express Route Circuits között.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="4bbe3-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="4bbe3-119">-AddressPrefixType</span></span>
<span data-ttu-id="4bbe3-120">Annak a címnek a családját adja meg, amelyhez a címelőtag tartozik.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbe3-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="4bbe3-121">-AuthorizationKey</span></span>
<span data-ttu-id="4bbe3-122">Engedélyezési kulcs társi Express Route Circuit-hez egy másik előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="4bbe3-123">A társ áramkörön az engedélyezés meglévő parancsokkal is létre lehet hozva.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="4bbe3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbe3-124">-DefaultProfile</span></span>
<span data-ttu-id="4bbe3-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bbe3-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bbe3-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4bbe3-127">A módosítva van az ExpressRoute-áramkör.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="4bbe3-128">Ez a **Get-AzExpressRouteCircuit** parancsmag által visszaadott Azure-objektum.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbe3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4bbe3-129">-Name</span></span>
<span data-ttu-id="4bbe3-130">A hozzáadni szükséges kapcsolatcsoport-kapcsolaterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-130">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbe3-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="4bbe3-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="4bbe3-132">A távoli kapcsolatcsoport magánjellegű társviszony-létesítésének erőforrás-azonosítója, amelynek társviszonya az aktuális áramkörrel fog.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbe3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bbe3-133">-Confirm</span></span>
<span data-ttu-id="4bbe3-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bbe3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbe3-135">-WhatIf</span></span>
<span data-ttu-id="4bbe3-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bbe3-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bbe3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbe3-138">CommonParameters</span></span>
<span data-ttu-id="4bbe3-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbe3-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbe3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bbe3-141">INPUTS</span></span>

### <span data-ttu-id="4bbe3-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bbe3-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4bbe3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4bbe3-143">System.String</span></span>

## <span data-ttu-id="4bbe3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bbe3-144">OUTPUTS</span></span>

### <span data-ttu-id="4bbe3-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bbe3-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4bbe3-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4bbe3-146">NOTES</span></span>

## <span data-ttu-id="4bbe3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bbe3-147">RELATED LINKS</span></span>

[<span data-ttu-id="4bbe3-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bbe3-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4bbe3-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bbe3-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4bbe3-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bbe3-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4bbe3-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bbe3-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="4bbe3-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bbe3-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
