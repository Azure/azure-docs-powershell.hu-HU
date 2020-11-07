---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 969d7c5f55d210cdff74066d08af50bbcc47181e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672927"
---
# <span data-ttu-id="6ff22-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ff22-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="6ff22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ff22-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff22-103">Azure ExpressRoute áramkört kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="6ff22-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ff22-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff22-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ff22-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff22-106">A **Get-AzureRmExpressRouteCircuit** parancsmag az ExpressRoute-áramköri objektumnak az előfizetésből való visszakeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6ff22-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="6ff22-107">A visszaadott áramkör-objektum a ExpressRoute-áramkörön működő többi parancsmaghoz is használható.</span><span class="sxs-lookup"><span data-stu-id="6ff22-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="6ff22-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6ff22-108">EXAMPLES</span></span>

### <span data-ttu-id="6ff22-109">Példa 1: a ExpressRoute-áramkör törlésének kérése</span><span class="sxs-lookup"><span data-stu-id="6ff22-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="6ff22-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ff22-110">PARAMETERS</span></span>

### <span data-ttu-id="6ff22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff22-111">-DefaultProfile</span></span>
<span data-ttu-id="6ff22-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ff22-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff22-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ff22-113">-Name</span></span>
<span data-ttu-id="6ff22-114">A ExpressRoute áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="6ff22-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6ff22-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff22-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ff22-116">Annak az erőforráscsoportnek a neve, amely a ExpressRoute áramkört tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ff22-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6ff22-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff22-117">CommonParameters</span></span>
<span data-ttu-id="6ff22-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ff22-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff22-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff22-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff22-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff22-120">INPUTS</span></span>

### <span data-ttu-id="6ff22-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff22-121">System.String</span></span>

## <span data-ttu-id="6ff22-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff22-122">OUTPUTS</span></span>

### <span data-ttu-id="6ff22-123">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ff22-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6ff22-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ff22-124">NOTES</span></span>

## <span data-ttu-id="6ff22-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ff22-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ff22-126">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ff22-126">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6ff22-127">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ff22-127">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6ff22-128">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ff22-128">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6ff22-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ff22-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
