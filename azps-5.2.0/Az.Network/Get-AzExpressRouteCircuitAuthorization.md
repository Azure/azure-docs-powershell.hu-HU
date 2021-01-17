---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323787"
---
# <span data-ttu-id="b87e7-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b87e7-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="b87e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b87e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b87e7-103">Információkat kap az ExpressRoute-kapcsolat kapcsolatengedélyeiről.</span><span class="sxs-lookup"><span data-stu-id="b87e7-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="b87e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b87e7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b87e7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b87e7-105">DESCRIPTION</span></span>
<span data-ttu-id="b87e7-106">A **Get-AzExpressRouteCircuitAuthorization** parancsmag információkat kap az ExpressRoute-áramkörhöz rendelt engedélyekről.</span><span class="sxs-lookup"><span data-stu-id="b87e7-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="b87e7-107">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz.</span><span class="sxs-lookup"><span data-stu-id="b87e7-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="b87e7-108">Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek olyan engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathatja a hálózatát az áramkörhöz (virtuális hálózatonként egy engedélyt).</span><span class="sxs-lookup"><span data-stu-id="b87e7-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="b87e7-109">Az engedélyezési kulcsok, valamint az engedélyezésre vonatkozó egyéb információk bármikor megtekinthetők a **Get-AzExpressRouteCircuitAuthorization futtatásával.**</span><span class="sxs-lookup"><span data-stu-id="b87e7-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="b87e7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b87e7-110">EXAMPLES</span></span>

### <span data-ttu-id="b87e7-111">1. példa: Az összes ExpressRoute-engedély kérése</span><span class="sxs-lookup"><span data-stu-id="b87e7-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="b87e7-112">Ezek a parancsok információt adnak az ExpressRoute-áramkörökkel társított ExpressRoute-engedélyekről.</span><span class="sxs-lookup"><span data-stu-id="b87e7-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="b87e7-113">Az első parancs a **Get-AzExpressRouteCircuit** parancsmaggal létrehoz egy ContosoCircuit nevű áramkörre hivatkozó objektumhivatkozást; ezt az objektumhivatkozást a következő változóban $Circuit.</span><span class="sxs-lookup"><span data-stu-id="b87e7-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="b87e7-114">A második parancs ezután az objektumhivatkozást és a **Get-AzExpressRouteCircuitAuthorization** parancsmagot használja a ContosoCircuithoz társított engedélyekre vonatkozó információk visszaadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="b87e7-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="b87e7-115">2. példa: Az összes ExpressRoute-engedély lekértése a Where-Object parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="b87e7-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="b87e7-116">Ezek a parancsok az 1. példában használt parancsok változatának jelképeznek.</span><span class="sxs-lookup"><span data-stu-id="b87e7-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="b87e7-117">Ebben az esetben azonban csak a használatra rendelkezésre álló engedélyekhez (például virtuális hálózathoz nem hozzárendelt engedélyekhez) kap adatokat a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b87e7-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="b87e7-118">Ehhez a 2. parancs visszaadja a kapcsolat kapcsolatengedélyezési adatait, és a **where-object** parancsmagba lesz becsökkentve.</span><span class="sxs-lookup"><span data-stu-id="b87e7-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="b87e7-119">**A Where-Object** ezután csak azokat az engedélyeket adja meg, *amelyeknél az AuthorizationUseStatus* tulajdonság Elérhetőre van állítva.</span><span class="sxs-lookup"><span data-stu-id="b87e7-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="b87e7-120">Ha csak azokat az engedélyeket sorolja fel, amelyek nem érhetők el, használja az alábbi szintaxist a Where záradékhoz: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="b87e7-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="b87e7-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b87e7-121">PARAMETERS</span></span>

### <span data-ttu-id="b87e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b87e7-122">-DefaultProfile</span></span>
<span data-ttu-id="b87e7-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b87e7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b87e7-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b87e7-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b87e7-125">Az ExpressRoute-kapcsolat kapcsolati engedélyének megadása.</span><span class="sxs-lookup"><span data-stu-id="b87e7-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="b87e7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b87e7-126">-Name</span></span>
<span data-ttu-id="b87e7-127">Annak az ExpressRoute-kapcsolati engedélynek a nevét adja meg, amelybe a parancsmagot beszerzi.</span><span class="sxs-lookup"><span data-stu-id="b87e7-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="b87e7-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="b87e7-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="b87e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87e7-129">CommonParameters</span></span>
<span data-ttu-id="b87e7-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b87e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87e7-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b87e7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87e7-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b87e7-132">INPUTS</span></span>

### <span data-ttu-id="b87e7-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b87e7-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b87e7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b87e7-134">OUTPUTS</span></span>

### <span data-ttu-id="b87e7-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b87e7-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="b87e7-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b87e7-136">NOTES</span></span>

## <span data-ttu-id="b87e7-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b87e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="b87e7-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b87e7-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b87e7-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b87e7-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b87e7-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b87e7-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b87e7-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b87e7-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
