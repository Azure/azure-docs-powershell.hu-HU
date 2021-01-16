---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354905"
---
# <span data-ttu-id="0ce87-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ce87-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0ce87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce87-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce87-103">ExpressRoute-kapcsolat kapcsolatengedélyt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0ce87-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="0ce87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ce87-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ce87-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ce87-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce87-106">A **New-AzExpressRouteCircuitAuthorization** parancsmag létrehoz egy áramkör-engedélyt, amely hozzáadható egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="0ce87-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="0ce87-107">Az ExpressRoute-áramkörök a nyilvános internet helyett egy kapcsolatszolgáltató használatával csatlakoztatják helyszíni hálózatát a Microsoft-felhőhöz.</span><span class="sxs-lookup"><span data-stu-id="0ce87-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="0ce87-108">Az ExpressRoute-áramkörök tulajdonosa akár 10 engedélyt is létrehozhat az egyes áramkörökhöz; ezek az engedélyek egy engedélyezési kulcsot hoznak létre, amelyet a virtuális hálózat tulajdonosa használva csatlakoztathat egy hálózatot az áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="0ce87-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="0ce87-109">Virtuális hálózatonként csak egy engedélyezési lehetőség használhatja.</span><span class="sxs-lookup"><span data-stu-id="0ce87-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="0ce87-110">Miután létrehozott egy ExpressRoute-áramkört, az **Add-AzExpressRouteCircuitAuthorization** segítségével adhat hozzá egy engedélyt az áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="0ce87-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="0ce87-111">Másik lehetőségként a **New-AzExpressRouteCircuitAuthorization** segítségével is létrehozhat egy olyan engedélyt, amely az áramkör létrehozásakor hozzáadható egy új áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="0ce87-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="0ce87-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ce87-112">EXAMPLES</span></span>

### <span data-ttu-id="0ce87-113">1. példa: Új kapcsolat kapcsolati engedély létrehozása</span><span class="sxs-lookup"><span data-stu-id="0ce87-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="0ce87-114">Ez a parancs létrehoz egy ContosoCircuitAuthorization nevű új áramkör-engedélyt, majd az objektumot egy $Authorization.</span><span class="sxs-lookup"><span data-stu-id="0ce87-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="0ce87-115">Fontos, hogy egy változóba mentse az objektumot: bár a **New-AzExpressRouteCircuitAuthorization** áramköri hitelesítést tud létrehozni, az adott engedélyt nem tudja hozzáadni egy áramköri útvonalhoz.</span><span class="sxs-lookup"><span data-stu-id="0ce87-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="0ce87-116">Ehelyett a $Authorization a New-AzExpressRouteCircuit egy vadonatúj ExpressRoute-áramkör létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="0ce87-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="0ce87-117">További információt a New-AzExpressRouteCircuit dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="0ce87-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="0ce87-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ce87-118">PARAMETERS</span></span>

### <span data-ttu-id="0ce87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce87-119">-DefaultProfile</span></span>
<span data-ttu-id="0ce87-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ce87-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce87-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0ce87-121">-Name</span></span>
<span data-ttu-id="0ce87-122">Az új ExpressRoute-kapcsolat kapcsolati engedélyének egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ce87-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="0ce87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce87-123">CommonParameters</span></span>
<span data-ttu-id="0ce87-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce87-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce87-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce87-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ce87-126">INPUTS</span></span>

### <span data-ttu-id="0ce87-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ce87-127">None</span></span>

## <span data-ttu-id="0ce87-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ce87-128">OUTPUTS</span></span>

### <span data-ttu-id="0ce87-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ce87-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0ce87-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ce87-130">NOTES</span></span>

## <span data-ttu-id="0ce87-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ce87-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ce87-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ce87-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0ce87-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ce87-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0ce87-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ce87-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

