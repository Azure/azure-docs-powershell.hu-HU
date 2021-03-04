---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918769"
---
# <span data-ttu-id="4d5d9-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4d5d9-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="4d5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5d9-103">ExpressRoute-kapcsolat kapcsolatengedélyt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="4d5d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d5d9-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d5d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="4d5d9-106">Az **Add-AzExpressRouteCircuitAuthorization** parancsmag engedélyt ad egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="4d5d9-107">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="4d5d9-108">Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek olyan engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathatja a hálózatát az áramkörhöz (virtuális hálózatonként egy engedélyt).</span><span class="sxs-lookup"><span data-stu-id="4d5d9-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="4d5d9-109">**Az Add-AzExpressRouteCircuitAuthorization** új engedélyt ad egy áramkörhöz, és ezzel egyidejűleg létrehozza a megfelelő engedélyezési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="4d5d9-110">Ezek a kulcsok bármikor megtekinthetők a Get-AzExpressRouteCircuitAuthorization parancsmag futtatásával, majd szükség esetén másolhatók és továbbíthatók a megfelelő hálózattulajdonosnak.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="4d5d9-111">Vegye figyelembe, hogy az **Add-AzExpressRouteCircuitAuthorization** futtatása után a kulcs aktiválásához Set-AzExpressRouteCircuit a Set-AzExpressRouteCircuit parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="4d5d9-112">Ha nem hívja fel a **Set-AzExpressRouteCircuitot,** a rendszer hozzáadja az engedélyt az áramkörhöz, de nem engedélyezi a használatát.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="4d5d9-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d5d9-113">EXAMPLES</span></span>

### <span data-ttu-id="4d5d9-114">1. példa: Engedély hozzáadása a megadott ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="4d5d9-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="4d5d9-115">A példában lévő parancsok új engedélyt adnak hozzá egy meglévő ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="4d5d9-116">Az első parancs **a Get-AzExpressRouteCircuit** segítségével létrehoz egy ContosoCircuit nevű áramkörre hivatkozó objektumhivatkozást.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="4d5d9-117">Ezt az objektumhivatkozást egy $Circuit.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="4d5d9-118">A második parancsban az **Add-AzExpressRouteCircuitAuthorization** parancsmaggal lehet új engedélyezési parancsot (ContosoCircuitAuthorization) hozzáadni az ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="4d5d9-119">Ez a parancs hozzáadja az engedélyt, de nem aktiválja azt.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="4d5d9-120">Az engedélyezéshez a példában az utolsó parancsban látható **Set-AzExpressRouteCircuit** szükséges.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="4d5d9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d5d9-121">PARAMETERS</span></span>

### <span data-ttu-id="4d5d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5d9-122">-DefaultProfile</span></span>
<span data-ttu-id="4d5d9-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d5d9-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4d5d9-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4d5d9-125">Megadja azt az ExpressRoute-áramkört, amelybe ez a parancsmag hozzáadja az engedélyt.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="4d5d9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4d5d9-126">-Name</span></span>
<span data-ttu-id="4d5d9-127">A hozzáadható kapcsolati engedély nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="4d5d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5d9-128">CommonParameters</span></span>
<span data-ttu-id="4d5d9-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5d9-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d5d9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5d9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d5d9-131">INPUTS</span></span>

### <span data-ttu-id="4d5d9-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4d5d9-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4d5d9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d5d9-133">OUTPUTS</span></span>

### <span data-ttu-id="4d5d9-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4d5d9-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4d5d9-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d5d9-135">NOTES</span></span>

## <span data-ttu-id="4d5d9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d5d9-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d5d9-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4d5d9-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4d5d9-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4d5d9-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4d5d9-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4d5d9-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4d5d9-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4d5d9-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4d5d9-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4d5d9-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
