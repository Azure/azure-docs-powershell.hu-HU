---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3d14a82cf387d85644870766cf92d1ede0c50b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837349"
---
# <span data-ttu-id="b36ea-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b36ea-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="b36ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b36ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b36ea-103">Információt kap a ExpressRoute-áramköri engedélyekről.</span><span class="sxs-lookup"><span data-stu-id="b36ea-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="b36ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b36ea-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b36ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b36ea-105">DESCRIPTION</span></span>
<span data-ttu-id="b36ea-106">A **Get-AzExpressRouteCircuitAuthorization** parancsmag információkat kap a ExpressRoute-áramkörhöz rendelt engedélyekről.</span><span class="sxs-lookup"><span data-stu-id="b36ea-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="b36ea-107">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="b36ea-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="b36ea-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz (virtuális hálózat esetén egy engedély).</span><span class="sxs-lookup"><span data-stu-id="b36ea-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="b36ea-109">Az engedélyezési kulcsok, valamint az engedélyezéssel kapcsolatos egyéb információk bármikor megtekinthetők a **Get-AzExpressRouteCircuitAuthorization** segítségével.</span><span class="sxs-lookup"><span data-stu-id="b36ea-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="b36ea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b36ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b36ea-111">Példa 1: az összes ExpressRoute-engedély beolvasása</span><span class="sxs-lookup"><span data-stu-id="b36ea-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="b36ea-112">Ezekkel a parancsokkal információt adhat meg az ExpressRoute-áramkörhöz társított összes ExpressRoute-engedélyről.</span><span class="sxs-lookup"><span data-stu-id="b36ea-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="b36ea-113">Az első parancs a **Get-AzExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű áramkör-hivatkozás létrehozásához; az objektum hivatkozását az $Circuit változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b36ea-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="b36ea-114">A második parancs ezután az Object Reference és a **Get-AzExpressRouteCircuitAuthorization** parancsmag segítségével visszaadja a ContosoCircuit társított engedélyekkel kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="b36ea-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="b36ea-115">2. példa: az összes ExpressRoute-engedély beszerzése az Where-Object parancsmag használatával</span><span class="sxs-lookup"><span data-stu-id="b36ea-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="b36ea-116">Ezek a parancsok a példaként használt parancsok variációját jelentik.</span><span class="sxs-lookup"><span data-stu-id="b36ea-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="b36ea-117">Ebben az esetben azonban csak azokat az engedélyeket adja vissza, amelyek használatra elérhetők (azaz a virtuális hálózathoz nem rendelt engedélyek esetén).</span><span class="sxs-lookup"><span data-stu-id="b36ea-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="b36ea-118">Ehhez az áramkör-engedélyezési információkat a 2-es parancs adja vissza, és a vezetékes a **Where-Object** parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b36ea-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="b36ea-119">**Where-objektum** : csak azokat az engedélyeket adja meg, amelyekben a *AuthorizationUseStatus* tulajdonság elérhető értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="b36ea-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="b36ea-120">Ha csak azokat az engedélyeket szeretné listázni, amelyek nem érhetők el, használja a WHERE záradék következő szintaxisát: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="b36ea-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="b36ea-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b36ea-121">PARAMETERS</span></span>

### <span data-ttu-id="b36ea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36ea-122">-DefaultProfile</span></span>
<span data-ttu-id="b36ea-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b36ea-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36ea-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b36ea-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b36ea-125">A ExpressRoute-áramkör engedélyezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="b36ea-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="b36ea-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b36ea-126">-Name</span></span>
<span data-ttu-id="b36ea-127">Annak a ExpressRoute-áramköri engedélynek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b36ea-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="b36ea-128">-Név "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="b36ea-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="b36ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36ea-129">CommonParameters</span></span>
<span data-ttu-id="b36ea-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b36ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36ea-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b36ea-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36ea-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b36ea-132">INPUTS</span></span>

### <span data-ttu-id="b36ea-133">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b36ea-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b36ea-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b36ea-134">OUTPUTS</span></span>

### <span data-ttu-id="b36ea-135">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b36ea-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="b36ea-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b36ea-136">NOTES</span></span>

## <span data-ttu-id="b36ea-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b36ea-137">RELATED LINKS</span></span>

[<span data-ttu-id="b36ea-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b36ea-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b36ea-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b36ea-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b36ea-140">Új – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b36ea-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b36ea-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b36ea-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
