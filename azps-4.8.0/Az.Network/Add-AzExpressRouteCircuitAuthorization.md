---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184904"
---
# <span data-ttu-id="c5e21-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c5e21-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="c5e21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5e21-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e21-103">ExpressRoute-áramkör-engedélyezést ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c5e21-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="c5e21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5e21-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5e21-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5e21-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e21-106">Az **Add-AzExpressRouteCircuitAuthorization** parancsmag egy ExpressRoute-áramkörhöz ad engedélyt.</span><span class="sxs-lookup"><span data-stu-id="c5e21-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="c5e21-107">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="c5e21-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="c5e21-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz (virtuális hálózat esetén egy engedély).</span><span class="sxs-lookup"><span data-stu-id="c5e21-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="c5e21-109">A **Add-AzExpressRouteCircuitAuthorization** új meghatalmazást ad hozzá egy áramkörhez, és egyidejűleg létrehozza a megfelelő engedélyezési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="c5e21-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="c5e21-110">Ezek a billentyűk bármikor megtekinthetők, ha futtatják az Get-AzExpressRouteCircuitAuthorization parancsmagot, és igény szerint át lehet őket másolni és továbbítani a megfelelő hálózati tulajdonosnak.</span><span class="sxs-lookup"><span data-stu-id="c5e21-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="c5e21-111">Felhívjuk a figyelmét arra, hogy a **AzExpressRouteCircuitAuthorization** futtatása után az Set-AzExpressRouteCircuit parancsmagot kell hívnia a kulcs aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="c5e21-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="c5e21-112">Ha nem hívja meg a **set-AzExpressRouteCircuit** , az engedélyt hozzáadja a program az áramkörhez, de nem lesz engedélyezve a használathoz.</span><span class="sxs-lookup"><span data-stu-id="c5e21-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="c5e21-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c5e21-113">EXAMPLES</span></span>

### <span data-ttu-id="c5e21-114">1. példa: engedély hozzáadása a megadott ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="c5e21-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="c5e21-115">Az ebben a példában szereplő parancsok új engedélyt adhatnak egy meglévő ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="c5e21-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="c5e21-116">Az első parancs a **Get-AzExpressRouteCircuit** használatával hoz létre egy ContosoCircuit nevű áramkört.</span><span class="sxs-lookup"><span data-stu-id="c5e21-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="c5e21-117">Az objektum hivatkozása $Circuit nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="c5e21-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="c5e21-118">A második parancsban a **Add-AzExpressRouteCircuitAuthorization** parancsmaggal új engedélyt (ContosoCircuitAuthorization) adhat a ExpressRoute áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="c5e21-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="c5e21-119">Ez a parancs hozzáadja az engedélyt, de nem aktiválja az engedélyt.</span><span class="sxs-lookup"><span data-stu-id="c5e21-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="c5e21-120">Az engedély aktiválásához a példában a végleges parancsban látható **set-AzExpressRouteCircuit** van szükség.</span><span class="sxs-lookup"><span data-stu-id="c5e21-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="c5e21-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5e21-121">PARAMETERS</span></span>

### <span data-ttu-id="c5e21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e21-122">-DefaultProfile</span></span>
<span data-ttu-id="c5e21-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5e21-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e21-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5e21-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c5e21-125">Azt a ExpressRoute-áramkört adja meg, amelyre a parancsmag hozzáadja az engedélyt.</span><span class="sxs-lookup"><span data-stu-id="c5e21-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="c5e21-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5e21-126">-Name</span></span>
<span data-ttu-id="c5e21-127">A hozzáadni kívánt áramkör-hitelesítés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5e21-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="c5e21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e21-128">CommonParameters</span></span>
<span data-ttu-id="c5e21-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5e21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e21-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e21-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e21-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5e21-131">INPUTS</span></span>

### <span data-ttu-id="c5e21-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5e21-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c5e21-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5e21-133">OUTPUTS</span></span>

### <span data-ttu-id="c5e21-134">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5e21-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c5e21-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5e21-135">NOTES</span></span>

## <span data-ttu-id="c5e21-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5e21-136">RELATED LINKS</span></span>

[<span data-ttu-id="c5e21-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5e21-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c5e21-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c5e21-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c5e21-139">Új – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c5e21-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c5e21-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c5e21-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c5e21-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5e21-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
