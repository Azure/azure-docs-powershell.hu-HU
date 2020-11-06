---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494842"
---
# <span data-ttu-id="cc676-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc676-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="cc676-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc676-102">SYNOPSIS</span></span>
<span data-ttu-id="cc676-103">Azure ExpressRoute áramkört kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="cc676-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc676-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc676-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc676-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc676-105">DESCRIPTION</span></span>
<span data-ttu-id="cc676-106">A **Get-AzureRmExpressRouteCircuit** parancsmag az ExpressRoute-áramköri objektumnak az előfizetésből való visszakeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="cc676-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="cc676-107">A visszaadott áramkör-objektum a ExpressRoute-áramkörön működő többi parancsmaghoz is használható.</span><span class="sxs-lookup"><span data-stu-id="cc676-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="cc676-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cc676-108">EXAMPLES</span></span>

### <span data-ttu-id="cc676-109">Példa 1: a ExpressRoute-áramkör törlésének kérése</span><span class="sxs-lookup"><span data-stu-id="cc676-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="cc676-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc676-110">PARAMETERS</span></span>

### <span data-ttu-id="cc676-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc676-111">-Name</span></span>
<span data-ttu-id="cc676-112">A ExpressRoute áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="cc676-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc676-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc676-113">-ResourceGroupName</span></span>
<span data-ttu-id="cc676-114">Annak az erőforráscsoportnek a neve, amely a ExpressRoute áramkört tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cc676-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc676-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc676-115">-DefaultProfile</span></span>
<span data-ttu-id="cc676-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc676-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc676-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc676-117">CommonParameters</span></span>
<span data-ttu-id="cc676-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc676-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc676-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc676-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc676-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc676-120">INPUTS</span></span>

## <span data-ttu-id="cc676-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc676-121">OUTPUTS</span></span>

### <span data-ttu-id="cc676-122">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc676-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cc676-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc676-123">NOTES</span></span>

## <span data-ttu-id="cc676-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc676-124">RELATED LINKS</span></span>

[<span data-ttu-id="cc676-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc676-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cc676-126">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc676-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cc676-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc676-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cc676-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc676-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
