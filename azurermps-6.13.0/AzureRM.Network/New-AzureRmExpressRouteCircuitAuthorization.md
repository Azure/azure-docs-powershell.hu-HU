---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 55c5fc3e534aa4239d6c466444a783b804ffc142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505339"
---
# <span data-ttu-id="1154f-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1154f-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="1154f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1154f-102">SYNOPSIS</span></span>
<span data-ttu-id="1154f-103">ExpressRoute-áramkör-engedélyezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1154f-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1154f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1154f-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1154f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1154f-105">DESCRIPTION</span></span>
<span data-ttu-id="1154f-106">A **New-AzureRmExpressRouteCircuitAuthorization** parancsmag olyan áramkör-hitelesítést hoz létre, amelyet hozzáadhat egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="1154f-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="1154f-107">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="1154f-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="1154f-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat a hálózat áramkörhöz való csatlakoztatásához.</span><span class="sxs-lookup"><span data-stu-id="1154f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="1154f-109">Egy virtuális hálózatban csak egy engedély használható.</span><span class="sxs-lookup"><span data-stu-id="1154f-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="1154f-110">Az ExpressRoute-áramkör létrehozása után a **AzureRmExpressRouteCircuitAuthorization** segítségével adhat hozzá engedélyt az adott áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="1154f-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="1154f-111">Azt is megteheti, hogy **új AzureRmExpressRouteCircuitAuthorization** is létrehozhat olyan engedélyeket, amelyek hozzáadhatók egy új áramkörhez az áramkör létrehozásának időpontjában.</span><span class="sxs-lookup"><span data-stu-id="1154f-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="1154f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1154f-112">EXAMPLES</span></span>

### <span data-ttu-id="1154f-113">1. példa: új áramkör-engedélyezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="1154f-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="1154f-114">Ez a parancs létrehoz egy ContosoCircuitAuthorization nevű új áramköri engedélyt, majd az objektumot egy $Authorization nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1154f-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="1154f-115">Az objektum változóra mentése fontos: Habár az **új AzureRmExpressRouteCircuitAuthorization** létrehozhatja az áramköri engedélyt, az nem vehető fel az áramköri útvonalra.</span><span class="sxs-lookup"><span data-stu-id="1154f-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="1154f-116">Az új ExpressRoute-áramkör létrehozásakor Ehelyett az $Authorization változót használja New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="1154f-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="1154f-117">További információt az New-AzureRmExpressRouteCircuit parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="1154f-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="1154f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1154f-118">PARAMETERS</span></span>

### <span data-ttu-id="1154f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1154f-119">-DefaultProfile</span></span>
<span data-ttu-id="1154f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1154f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1154f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1154f-121">-Name</span></span>
<span data-ttu-id="1154f-122">Az új ExpressRoute-adatáramkör-engedélyezés egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1154f-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="1154f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1154f-123">CommonParameters</span></span>
<span data-ttu-id="1154f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1154f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1154f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1154f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1154f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1154f-126">INPUTS</span></span>

### <span data-ttu-id="1154f-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="1154f-127">None</span></span>

## <span data-ttu-id="1154f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1154f-128">OUTPUTS</span></span>

### <span data-ttu-id="1154f-129">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1154f-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="1154f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1154f-130">NOTES</span></span>

## <span data-ttu-id="1154f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1154f-131">RELATED LINKS</span></span>

[<span data-ttu-id="1154f-132">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1154f-132">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1154f-133">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1154f-133">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1154f-134">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1154f-134">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

