---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: af8490ab242919d44b0b1b47c9cab92674e9df9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680860"
---
# <span data-ttu-id="e9ceb-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e9ceb-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="e9ceb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ceb-103">A meglévő ExpressRoute-konfiguráció engedélyezésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9ceb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9ceb-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9ceb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9ceb-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ceb-106">A **Remove-AzureRmExpressRouteCircuitAuthorization** parancsmag eltávolítja a ExpressRoute-áramkörhez rendelt engedélyt.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="e9ceb-107">A ExpressRoute-áramkörök a helyszíni hálózatokat az Azure rendszerhez csatlakozva a nyilvános Internet helyett a szolgáltatót használják.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="e9ceb-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="e9ceb-109">Virtuális hálózatban csak egy engedély lehet.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="e9ceb-110">Az áramkör tulajdonosa azonban bármikor eltávolíthatja a **AzureRmExpressRouteCircuitAuthorization** a virtuális hálózathoz rendelt engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="e9ceb-111">Amikor ez történik, a megfelelő virtuális hálózat már nem tudja használni a ExpressRoute áramkört az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="e9ceb-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e9ceb-112">EXAMPLES</span></span>

### <span data-ttu-id="e9ceb-113">1. példa: ExpressRoute áramkör-engedélyezés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e9ceb-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="e9ceb-114">Ez a példa egy ExpressRoute-áramkörből eltávolítja az áramkör-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="e9ceb-115">Az első parancs a **Get-AzureRmExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű ExpressRoute-áramkörhöz tartozó objektum-hivatkozás létrehozásához, és az eredményt az $Circuit nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="e9ceb-116">A második parancs az áramkör-engedélyezési ContosoCircuitAuthorization az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="e9ceb-117">A harmadik parancs az Set-AzureRmExpressRouteCircuit parancsmagot használja a $Circuit változóban tárolt ExpressRoute-áramkör eltávolításának megerősítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="e9ceb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9ceb-118">PARAMETERS</span></span>

### <span data-ttu-id="e9ceb-119">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e9ceb-119">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e9ceb-120">A parancsmag által eltávolított ExpressRouteCircuit objektum meghatározása.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-120">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9ceb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9ceb-121">-Name</span></span>
<span data-ttu-id="e9ceb-122">Annak az áramkör-engedélynek a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-122">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9ceb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ceb-123">-DefaultProfile</span></span>
<span data-ttu-id="e9ceb-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9ceb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ceb-125">CommonParameters</span></span>
<span data-ttu-id="e9ceb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9ceb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ceb-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ceb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ceb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9ceb-128">INPUTS</span></span>

### <span data-ttu-id="e9ceb-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e9ceb-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e9ceb-130">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum pipeline-példányait fogadja el.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="e9ceb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9ceb-131">OUTPUTS</span></span>

### <span data-ttu-id="e9ceb-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e9ceb-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e9ceb-133">Ez a parancsmag módosítja a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum meglévő példányait.</span><span class="sxs-lookup"><span data-stu-id="e9ceb-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="e9ceb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9ceb-134">NOTES</span></span>

## <span data-ttu-id="e9ceb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9ceb-135">RELATED LINKS</span></span>

[<span data-ttu-id="e9ceb-136">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e9ceb-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e9ceb-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e9ceb-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e9ceb-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e9ceb-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e9ceb-139">Új – AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e9ceb-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e9ceb-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e9ceb-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
