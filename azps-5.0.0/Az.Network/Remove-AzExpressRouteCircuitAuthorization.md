---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195353"
---
# <span data-ttu-id="a7d8d-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a7d8d-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="a7d8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d8d-103">A meglévő ExpressRoute-konfiguráció engedélyezésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="a7d8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7d8d-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d8d-106">A **Remove-AzExpressRouteCircuitAuthorization** parancsmag eltávolítja a ExpressRoute-áramkörhez rendelt engedélyt.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="a7d8d-107">A ExpressRoute-áramkörök a helyszíni hálózatokat az Azure rendszerhez csatlakozva a nyilvános Internet helyett a szolgáltatót használják.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a7d8d-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="a7d8d-109">Virtuális hálózatban csak egy engedély lehet.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="a7d8d-110">Az áramkör tulajdonosa azonban bármikor eltávolíthatja a **AzExpressRouteCircuitAuthorization** a virtuális hálózathoz rendelt engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="a7d8d-111">Amikor ez történik, a megfelelő virtuális hálózat már nem tudja használni a ExpressRoute áramkört az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="a7d8d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a7d8d-112">EXAMPLES</span></span>

### <span data-ttu-id="a7d8d-113">1. példa: ExpressRoute áramkör-engedélyezés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a7d8d-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="a7d8d-114">Ez a példa egy ExpressRoute-áramkörből eltávolítja az áramkör-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="a7d8d-115">Az első parancs a **Get-AzExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű ExpressRoute-áramkörhöz tartozó objektum-hivatkozás létrehozásához, és az eredményt az $Circuit nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="a7d8d-116">A második parancs az áramkör-engedélyezési ContosoCircuitAuthorization az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="a7d8d-117">A harmadik parancs az Set-AzExpressRouteCircuit parancsmagot használja a $Circuit változóban tárolt ExpressRoute-áramkör eltávolításának megerősítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="a7d8d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7d8d-118">PARAMETERS</span></span>

### <span data-ttu-id="a7d8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d8d-119">-DefaultProfile</span></span>
<span data-ttu-id="a7d8d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d8d-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7d8d-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a7d8d-122">A parancsmag által eltávolított ExpressRouteCircuit objektum meghatározása.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7d8d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7d8d-123">-Name</span></span>
<span data-ttu-id="a7d8d-124">Annak az áramkör-engedélynek a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7d8d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d8d-125">CommonParameters</span></span>
<span data-ttu-id="a7d8d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7d8d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d8d-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d8d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d8d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7d8d-128">INPUTS</span></span>

### <span data-ttu-id="a7d8d-129">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7d8d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a7d8d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7d8d-130">OUTPUTS</span></span>

### <span data-ttu-id="a7d8d-131">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7d8d-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a7d8d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7d8d-132">NOTES</span></span>

## <span data-ttu-id="a7d8d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7d8d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7d8d-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a7d8d-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a7d8d-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7d8d-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a7d8d-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a7d8d-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a7d8d-137">Új – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a7d8d-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a7d8d-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7d8d-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
