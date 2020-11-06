---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3aed1a20a8a5878819ea3634ff5d31babba3261c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496444"
---
# <span data-ttu-id="fc07f-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fc07f-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="fc07f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc07f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc07f-103">Információt kap a ExpressRoute-áramköri engedélyekről.</span><span class="sxs-lookup"><span data-stu-id="fc07f-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc07f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc07f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc07f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc07f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc07f-106">A **Get-AzureRmExpressRouteCircuitAuthorization** parancsmag információkat kap a ExpressRoute-áramkörhöz rendelt engedélyekről.</span><span class="sxs-lookup"><span data-stu-id="fc07f-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="fc07f-107">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="fc07f-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="fc07f-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat az áramkörhöz való csatlakozáshoz (virtuális hálózat esetén egy engedély).</span><span class="sxs-lookup"><span data-stu-id="fc07f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="fc07f-109">Az engedélyezési kulcsok, valamint az engedélyezéssel kapcsolatos egyéb információk bármikor megtekinthetők a **Get-AzureRmExpressRouteCircuitAuthorization** segítségével.</span><span class="sxs-lookup"><span data-stu-id="fc07f-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="fc07f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fc07f-110">EXAMPLES</span></span>

### <span data-ttu-id="fc07f-111">Példa 1: az összes ExpressRoute-engedély beolvasása</span><span class="sxs-lookup"><span data-stu-id="fc07f-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="fc07f-112">Ezekkel a parancsokkal információt adhat meg az ExpressRoute-áramkörhöz társított összes ExpressRoute-engedélyről.</span><span class="sxs-lookup"><span data-stu-id="fc07f-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="fc07f-113">Az első parancs a **Get-AzureRmExpressRouteCircuit** parancsmagot használja a ContosoCircuit nevű áramkör-hivatkozás létrehozásához; az objektum hivatkozását az $Circuit változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc07f-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="fc07f-114">A második parancs ezután az Object Reference és a **Get-AzureRmExpressRouteCircuitAuthorization** parancsmag segítségével visszaadja a ContosoCircuit társított engedélyekkel kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="fc07f-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="fc07f-115">2. példa: az összes ExpressRoute-engedély beszerzése az Where-Object parancsmag használatával</span><span class="sxs-lookup"><span data-stu-id="fc07f-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="fc07f-116">Ezek a parancsok a példaként használt parancsok variációját jelentik.</span><span class="sxs-lookup"><span data-stu-id="fc07f-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="fc07f-117">Ebben az esetben azonban csak azokat az engedélyeket adja vissza, amelyek használatra elérhetők (azaz a virtuális hálózathoz nem rendelt engedélyek esetén).</span><span class="sxs-lookup"><span data-stu-id="fc07f-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="fc07f-118">Ehhez az áramkör-engedélyezési információkat a 2-es parancs adja vissza, és a vezetékes a **Where-Object** parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fc07f-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="fc07f-119">**Where-objektum** : csak azokat az engedélyeket adja meg, amelyekben a *AuthorizationUseStatus* tulajdonság elérhető értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="fc07f-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="fc07f-120">Ha csak azokat az engedélyeket szeretné listázni, amelyek nem érhetők el, használja a WHERE záradék következő szintaxisát:</span><span class="sxs-lookup"><span data-stu-id="fc07f-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="fc07f-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc07f-121">PARAMETERS</span></span>

### <span data-ttu-id="fc07f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc07f-122">-DefaultProfile</span></span>
<span data-ttu-id="fc07f-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc07f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc07f-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fc07f-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="fc07f-125">A ExpressRoute-áramkör engedélyezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc07f-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="fc07f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc07f-126">-Name</span></span>
<span data-ttu-id="fc07f-127">Annak a ExpressRoute-áramköri engedélynek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="fc07f-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="fc07f-128">-Név "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="fc07f-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="fc07f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc07f-129">CommonParameters</span></span>
<span data-ttu-id="fc07f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc07f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc07f-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc07f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc07f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc07f-132">INPUTS</span></span>

### <span data-ttu-id="fc07f-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fc07f-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="fc07f-134">A **Get-AzureRmExpressRouteCircuitAuthorization** elfogadja a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit** objektum csővezetékes példányait.</span><span class="sxs-lookup"><span data-stu-id="fc07f-134">**Get-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="fc07f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc07f-135">OUTPUTS</span></span>

### <span data-ttu-id="fc07f-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fc07f-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="fc07f-137">A **Get-AzureRmExpressRouteCircuitAuthorization** a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization** objektum példányait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fc07f-137">**Get-AzureRmExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="fc07f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc07f-138">NOTES</span></span>

## <span data-ttu-id="fc07f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc07f-139">RELATED LINKS</span></span>

[<span data-ttu-id="fc07f-140">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fc07f-140">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="fc07f-141">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fc07f-141">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fc07f-142">Új – AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fc07f-142">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="fc07f-143">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fc07f-143">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
