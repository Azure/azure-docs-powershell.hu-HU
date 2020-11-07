---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: ef00e209b030ed4a05ad29ccb3e768df090ea8ee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841165"
---
# <span data-ttu-id="0a0bd-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0a0bd-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0a0bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0bd-103">A meglévő ExpressRoute-konfiguráció engedélyezésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="0a0bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a0bd-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a0bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a0bd-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0bd-106">A **Remove-AzExpressRouteCircuitAuthorization** parancsmag eltávolítja a ExpressRoute-áramkörhez rendelt engedélyt.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="0a0bd-107">A ExpressRoute-áramkörök a helyszíni hálózatokat az Azure rendszerhez csatlakozva a nyilvános Internet helyett a szolgáltatót használják.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="0a0bd-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="0a0bd-109">Virtuális hálózatban csak egy engedély lehet.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="0a0bd-110">Az áramkör tulajdonosa azonban bármikor eltávolíthatja a **AzExpressRouteCircuitAuthorization** a virtuális hálózathoz rendelt engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="0a0bd-111">Amikor ez történik, a megfelelő virtuális hálózat már nem tudja használni a ExpressRoute áramkört az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="0a0bd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0a0bd-112">EXAMPLES</span></span>

### <span data-ttu-id="0a0bd-113">1. példa: ExpressRoute áramkör-engedélyezés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a0bd-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="0a0bd-114">Ez a példa egy ExpressRoute-áramkörből eltávolítja az áramkör-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="0a0bd-115">Az első parancs a **Get-AzExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű ExpressRoute-áramkörhöz tartozó objektum-hivatkozás létrehozásához, és az eredményt az $Circuit nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="0a0bd-116">A második parancs az áramkör-engedélyezési ContosoCircuitAuthorization az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="0a0bd-117">A harmadik parancs az Set-AzExpressRouteCircuit parancsmagot használja a $Circuit változóban tárolt ExpressRoute-áramkör eltávolításának megerősítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="0a0bd-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a0bd-118">PARAMETERS</span></span>

### <span data-ttu-id="0a0bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0bd-119">-DefaultProfile</span></span>
<span data-ttu-id="0a0bd-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a0bd-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0a0bd-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0a0bd-122">A parancsmag által eltávolított ExpressRouteCircuit objektum meghatározása.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a0bd-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a0bd-123">-Name</span></span>
<span data-ttu-id="0a0bd-124">Annak az áramkör-engedélynek a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a0bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0bd-125">CommonParameters</span></span>
<span data-ttu-id="0a0bd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a0bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0bd-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0bd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0bd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a0bd-128">INPUTS</span></span>

### <span data-ttu-id="0a0bd-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0a0bd-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="0a0bd-130">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum pipeline-példányait fogadja el.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="0a0bd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a0bd-131">OUTPUTS</span></span>

### <span data-ttu-id="0a0bd-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0a0bd-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="0a0bd-133">Ez a parancsmag módosítja a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum meglévő példányait.</span><span class="sxs-lookup"><span data-stu-id="0a0bd-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="0a0bd-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a0bd-134">NOTES</span></span>

## <span data-ttu-id="0a0bd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a0bd-135">RELATED LINKS</span></span>

[<span data-ttu-id="0a0bd-136">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0a0bd-136">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0a0bd-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0a0bd-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0a0bd-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0a0bd-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0a0bd-139">Új – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0a0bd-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0a0bd-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0a0bd-140">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
