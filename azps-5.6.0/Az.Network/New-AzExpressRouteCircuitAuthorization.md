---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941081"
---
# <span data-ttu-id="813dd-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="813dd-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="813dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="813dd-102">SYNOPSIS</span></span>
<span data-ttu-id="813dd-103">ExpressRoute-kapcsolat kapcsolatengedélyt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="813dd-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="813dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="813dd-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="813dd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="813dd-105">DESCRIPTION</span></span>
<span data-ttu-id="813dd-106">A **New-AzExpressRouteCircuitAuthorization** parancsmag létrehoz egy áramkör-engedélyt, amely hozzáadható egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="813dd-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="813dd-107">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz.</span><span class="sxs-lookup"><span data-stu-id="813dd-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="813dd-108">Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek egy engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathat egy hálózatot az áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="813dd-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="813dd-109">Virtuális hálózatonként csak egy engedélyezési lehetőség használhatja.</span><span class="sxs-lookup"><span data-stu-id="813dd-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="813dd-110">Miután létrehozott egy ExpressRoute-áramkört, az **Add-AzExpressRouteCircuitAuthorization** segítségével adhat hozzá egy engedélyt az áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="813dd-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="813dd-111">Másik lehetőségként használhatja a **New-AzExpressRouteCircuitAuthorization** hitelesítést, amely az áramkör létrehozásakor hozzáadható egy új áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="813dd-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="813dd-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="813dd-112">EXAMPLES</span></span>

### <span data-ttu-id="813dd-113">1. példa: Új kapcsolat kapcsolati engedély létrehozása</span><span class="sxs-lookup"><span data-stu-id="813dd-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="813dd-114">Ez a parancs létrehoz egy ContosoCircuitAuthorization nevű új kapcsolati kapcsolati engedélyt, majd az objektumot egy $Authorization.</span><span class="sxs-lookup"><span data-stu-id="813dd-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="813dd-115">Fontos, hogy egy változóba mentse az objektumot: bár a **New-AzExpressRouteCircuitAuthorization** áramköri hitelesítést tud létrehozni, az adott engedélyt nem tudja hozzáadni egy áramköri útvonalhoz.</span><span class="sxs-lookup"><span data-stu-id="813dd-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="813dd-116">Ehelyett a $Authorization a New-AzExpressRouteCircuit egy vadonatúj ExpressRoute-áramkör létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="813dd-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="813dd-117">További információt a New-AzExpressRouteCircuit dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="813dd-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="813dd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="813dd-118">PARAMETERS</span></span>

### <span data-ttu-id="813dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813dd-119">-DefaultProfile</span></span>
<span data-ttu-id="813dd-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="813dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="813dd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="813dd-121">-Name</span></span>
<span data-ttu-id="813dd-122">Az új ExpressRoute-kapcsolat kapcsolati engedélyének egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="813dd-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="813dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813dd-123">CommonParameters</span></span>
<span data-ttu-id="813dd-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813dd-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813dd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813dd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="813dd-126">INPUTS</span></span>

### <span data-ttu-id="813dd-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="813dd-127">None</span></span>

## <span data-ttu-id="813dd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="813dd-128">OUTPUTS</span></span>

### <span data-ttu-id="813dd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="813dd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="813dd-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="813dd-130">NOTES</span></span>

## <span data-ttu-id="813dd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="813dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="813dd-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="813dd-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="813dd-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="813dd-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="813dd-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="813dd-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

