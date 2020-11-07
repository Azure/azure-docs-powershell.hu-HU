---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849141"
---
# <span data-ttu-id="18eed-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="18eed-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="18eed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18eed-102">SYNOPSIS</span></span>
<span data-ttu-id="18eed-103">ExpressRoute-áramkör-engedélyezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="18eed-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18eed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18eed-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18eed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18eed-105">DESCRIPTION</span></span>
<span data-ttu-id="18eed-106">A **New-AzureRmExpressRouteCircuitAuthorization** parancsmag olyan áramkör-hitelesítést hoz létre, amelyet hozzáadhat egy ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="18eed-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="18eed-107">A ExpressRoute-áramkörök a nyilvános Internet helyett a Microsoft Cloud-hoz csatlakoznak a helyszíni hálózatról.</span><span class="sxs-lookup"><span data-stu-id="18eed-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="18eed-108">Egy ExpressRoute-áramkör tulajdonosa minden áramkörhöz több mint 10 engedélyt hozhat létre; Ezek az engedélyek létrehoznak egy olyan engedélyezési kulcsot, amelyet egy virtuális hálózat tulajdonosa használhat a hálózat áramkörhöz való csatlakoztatásához.</span><span class="sxs-lookup"><span data-stu-id="18eed-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="18eed-109">Egy virtuális hálózatban csak egy engedély használható.</span><span class="sxs-lookup"><span data-stu-id="18eed-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="18eed-110">Az ExpressRoute-áramkör létrehozása után a **AzureRmExpressRouteCircuitAuthorization** segítségével adhat hozzá engedélyt az adott áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="18eed-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="18eed-111">Azt is megteheti, hogy **új AzureRmExpressRouteCircuitAuthorization** is létrehozhat olyan engedélyeket, amelyek hozzáadhatók egy új áramkörhez az áramkör létrehozásának időpontjában.</span><span class="sxs-lookup"><span data-stu-id="18eed-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="18eed-112">Példák</span><span class="sxs-lookup"><span data-stu-id="18eed-112">EXAMPLES</span></span>

### <span data-ttu-id="18eed-113">1. példa: új áramkör-engedélyezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="18eed-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="18eed-114">Ez a parancs létrehoz egy ContosoCircuitAuthorization nevű új áramköri engedélyt, majd az objektumot egy $Authorization nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18eed-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="18eed-115">Az objektum változóra mentése fontos: Habár az **új AzureRmExpressRouteCircuitAuthorization** létrehozhatja az áramköri engedélyt, az nem vehető fel az áramköri útvonalra.</span><span class="sxs-lookup"><span data-stu-id="18eed-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="18eed-116">Az új ExpressRoute-áramkör létrehozásakor Ehelyett az $Authorization változót használja New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="18eed-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="18eed-117">További információt az New-AzureRmExpressRouteCircuit parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="18eed-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="18eed-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18eed-118">PARAMETERS</span></span>

### <span data-ttu-id="18eed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18eed-119">-DefaultProfile</span></span>
<span data-ttu-id="18eed-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18eed-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18eed-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18eed-121">-Name</span></span>
<span data-ttu-id="18eed-122">Az új ExpressRoute-adatáramkör-engedélyezés egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18eed-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eed-123">CommonParameters</span></span>
<span data-ttu-id="18eed-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18eed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eed-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18eed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eed-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18eed-126">INPUTS</span></span>

### <span data-ttu-id="18eed-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="18eed-127">None</span></span>
<span data-ttu-id="18eed-128">Ez a parancsmag nem fogadja el a csővezetékes bevitelt.</span><span class="sxs-lookup"><span data-stu-id="18eed-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="18eed-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18eed-129">OUTPUTS</span></span>

### <span data-ttu-id="18eed-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="18eed-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="18eed-131">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization** objektum példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="18eed-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="18eed-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18eed-132">NOTES</span></span>

## <span data-ttu-id="18eed-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18eed-133">RELATED LINKS</span></span>

[<span data-ttu-id="18eed-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="18eed-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="18eed-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="18eed-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="18eed-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="18eed-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

