---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378795"
---
# <span data-ttu-id="697fd-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="697fd-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="697fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="697fd-102">SYNOPSIS</span></span>
<span data-ttu-id="697fd-103">Eltávolít egy meglévő ExpressRoute-konfigurációengedélyt.</span><span class="sxs-lookup"><span data-stu-id="697fd-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="697fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="697fd-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="697fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="697fd-105">DESCRIPTION</span></span>
<span data-ttu-id="697fd-106">A **Remove-AzExpressRouteCircuitAuthorization** parancsmag eltávolítja az ExpressRoute-áramkörhöz rendelt engedélyt.</span><span class="sxs-lookup"><span data-stu-id="697fd-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="697fd-107">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="697fd-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="697fd-108">Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek olyan engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathatja a hálózatát az áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="697fd-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="697fd-109">Virtuális hálózatonként csak egy engedélyezési lehetőség lehet.</span><span class="sxs-lookup"><span data-stu-id="697fd-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="697fd-110">A kapcsolatcsoport tulajdonosa azonban bármikor használhatja a **Remove-AzExpressRouteCircuitAuthorization** kapcsolót a virtuális hálózathoz rendelt engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="697fd-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="697fd-111">Ilyen esetben a megfelelő virtuális hálózat már nem tudja használni az ExpressRoute-áramkört az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="697fd-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="697fd-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="697fd-112">EXAMPLES</span></span>

### <span data-ttu-id="697fd-113">1. példa: Áramkör-hitelesítés eltávolítása Egy ExpressRoute-áramkörből</span><span class="sxs-lookup"><span data-stu-id="697fd-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="697fd-114">Ez a példa eltávolítja az áramkör-hitelesítést egy ExpressRoute-áramkörből.</span><span class="sxs-lookup"><span data-stu-id="697fd-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="697fd-115">Az első parancs a **Get-AzExpressRouteCircuit** parancsmag segítségével létrehoz egy ContosoCircuit nevű ExpressRoute-áramkörre való objektumhivatkozást, és az eredményt a $Circuit.</span><span class="sxs-lookup"><span data-stu-id="697fd-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="697fd-116">A második parancs az eltávolításra használt ContosoCircuitAuthorization áramkör-hitelesítést jelöli.</span><span class="sxs-lookup"><span data-stu-id="697fd-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="697fd-117">A harmadik parancs a Set-AzExpressRouteCircuit parancsmag segítségével erősítse meg a $Circuit ExpressRoute-áramkör eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="697fd-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="697fd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="697fd-118">PARAMETERS</span></span>

### <span data-ttu-id="697fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="697fd-119">-DefaultProfile</span></span>
<span data-ttu-id="697fd-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="697fd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="697fd-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="697fd-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="697fd-122">A parancsmag által eltávolított ExpressRouteCircuit-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="697fd-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="697fd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="697fd-123">-Name</span></span>
<span data-ttu-id="697fd-124">A parancsmag által eltávolított kapcsolati engedély nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="697fd-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="697fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="697fd-125">CommonParameters</span></span>
<span data-ttu-id="697fd-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="697fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="697fd-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="697fd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="697fd-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="697fd-128">INPUTS</span></span>

### <span data-ttu-id="697fd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="697fd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="697fd-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="697fd-130">OUTPUTS</span></span>

### <span data-ttu-id="697fd-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="697fd-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="697fd-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="697fd-132">NOTES</span></span>

## <span data-ttu-id="697fd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="697fd-133">RELATED LINKS</span></span>

[<span data-ttu-id="697fd-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="697fd-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="697fd-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="697fd-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="697fd-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="697fd-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="697fd-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="697fd-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="697fd-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="697fd-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
