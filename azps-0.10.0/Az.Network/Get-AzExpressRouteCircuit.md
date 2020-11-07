---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841677"
---
# <span data-ttu-id="4e59a-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e59a-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4e59a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e59a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e59a-103">Azure ExpressRoute áramkört kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="4e59a-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="4e59a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e59a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e59a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e59a-105">DESCRIPTION</span></span>
<span data-ttu-id="4e59a-106">A **Get-AzExpressRouteCircuit** parancsmag az ExpressRoute-áramköri objektumnak az előfizetésből való visszakeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="4e59a-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="4e59a-107">A visszaadott áramkör-objektum a ExpressRoute-áramkörön működő többi parancsmaghoz is használható.</span><span class="sxs-lookup"><span data-stu-id="4e59a-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="4e59a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4e59a-108">EXAMPLES</span></span>

### <span data-ttu-id="4e59a-109">Példa 1: a ExpressRoute-áramkör törlésének kérése</span><span class="sxs-lookup"><span data-stu-id="4e59a-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="4e59a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e59a-110">PARAMETERS</span></span>

### <span data-ttu-id="4e59a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e59a-111">-DefaultProfile</span></span>
<span data-ttu-id="4e59a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e59a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e59a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e59a-113">-Name</span></span>
<span data-ttu-id="4e59a-114">A ExpressRoute áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="4e59a-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e59a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e59a-116">Annak az erőforráscsoportnek a neve, amely a ExpressRoute áramkört tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4e59a-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e59a-117">CommonParameters</span></span>
<span data-ttu-id="4e59a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e59a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e59a-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e59a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e59a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e59a-120">INPUTS</span></span>

## <span data-ttu-id="4e59a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e59a-121">OUTPUTS</span></span>

### <span data-ttu-id="4e59a-122">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e59a-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4e59a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e59a-123">NOTES</span></span>

## <span data-ttu-id="4e59a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e59a-124">RELATED LINKS</span></span>

[<span data-ttu-id="4e59a-125">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e59a-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e59a-126">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e59a-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e59a-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e59a-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e59a-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e59a-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
