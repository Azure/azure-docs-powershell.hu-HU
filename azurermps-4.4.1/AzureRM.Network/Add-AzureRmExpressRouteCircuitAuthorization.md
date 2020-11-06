---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 03b9e64970be7f3d3876a3d04f26b11ac24dd8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502676"
---
# <span data-ttu-id="d6b0a-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d6b0a-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="d6b0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b0a-103">ExpressRoute-áramkör-engedélyezést ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6b0a-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b0a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6b0a-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b0a-106">Az **Add-AzureRmExpressRouteCircuitAuthorization** parancsmag egy ExpressRoute-áramkörhöz ad engedélyt.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="d6b0a-107">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="d6b0a-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz (virtuális hálózat esetén egy engedély).</span><span class="sxs-lookup"><span data-stu-id="d6b0a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="d6b0a-109">A **Add-AzureRmExpressRouteCircuitAuthorization** új meghatalmazást ad hozzá egy áramkörhez, és egyidejűleg létrehozza a megfelelő engedélyezési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="d6b0a-110">Ezek a billentyűk bármikor megtekinthetők, ha futtatják az Get-AzureRmExpressRouteCircuitAuthorization parancsmagot, és igény szerint át lehet őket másolni és továbbítani a megfelelő hálózati tulajdonosnak.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="d6b0a-111">Felhívjuk a figyelmét arra, hogy a **AzureRmExpressRouteCircuitAuthorization** futtatása után az Set-AzureRmExpressRouteCircuit parancsmagot kell hívnia a kulcs aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="d6b0a-112">Ha nem hívja meg a **set-AzureRmExpressRouteCircuit** , az engedélyt hozzáadja a program az áramkörhez, de nem lesz engedélyezve a használathoz.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="d6b0a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d6b0a-113">EXAMPLES</span></span>

### <span data-ttu-id="d6b0a-114">1. példa: engedély hozzáadása a megadott ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="d6b0a-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="d6b0a-115">Az ebben a példában szereplő parancsok új engedélyt adhatnak egy meglévő ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="d6b0a-116">Az első parancs a **Get-AzureRmExpressRouteCircuit** használatával hoz létre egy ContosoCircuit nevű áramkört.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="d6b0a-117">Az objektum hivatkozása $Circuit nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="d6b0a-118">A második parancsban a **Add-AzureRmExpressRouteCircuitAuthorization** parancsmaggal új engedélyt (ContosoCircuitAuthorization) adhat a ExpressRoute áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="d6b0a-119">Ez a parancs hozzáadja az engedélyt, de nem aktiválja az engedélyt.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="d6b0a-120">Az engedély aktiválásához a példában a végleges parancsban látható **set-AzureRmExpressRouteCircuit** van szükség.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="d6b0a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6b0a-121">PARAMETERS</span></span>

### <span data-ttu-id="d6b0a-122">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d6b0a-122">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d6b0a-123">Azt a ExpressRoute-áramkört adja meg, amelyre a parancsmag hozzáadja az engedélyt.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-123">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="d6b0a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6b0a-124">-Name</span></span>
<span data-ttu-id="d6b0a-125">A hozzáadni kívánt áramkör-hitelesítés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-125">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="d6b0a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b0a-126">-DefaultProfile</span></span>
<span data-ttu-id="d6b0a-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b0a-128">CommonParameters</span></span>
<span data-ttu-id="d6b0a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6b0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b0a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b0a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b0a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6b0a-131">INPUTS</span></span>

### <span data-ttu-id="d6b0a-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d6b0a-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d6b0a-133">A **Add-AzureRmExpressRouteCircuitAuthorization** elfogadja a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum csővezetékes példányait.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="d6b0a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6b0a-134">OUTPUTS</span></span>

### <span data-ttu-id="d6b0a-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d6b0a-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d6b0a-136">A **Add-AzureRmExpressRouteCircuitAuthorization** módosítja a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum példányait.</span><span class="sxs-lookup"><span data-stu-id="d6b0a-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="d6b0a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6b0a-137">NOTES</span></span>

## <span data-ttu-id="d6b0a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6b0a-138">RELATED LINKS</span></span>

[<span data-ttu-id="d6b0a-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d6b0a-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d6b0a-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d6b0a-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d6b0a-141">Új – AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d6b0a-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d6b0a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d6b0a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d6b0a-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d6b0a-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)