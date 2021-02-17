---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154107"
---
# <span data-ttu-id="d8b80-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="d8b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8b80-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b80-103">Módosít egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="d8b80-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d8b80-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8b80-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b80-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8b80-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b80-106">A **Set-AzExpressRouteCircuit** parancsmag menti a módosított ExpressRoute-áramkört az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="d8b80-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="d8b80-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8b80-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b80-108">1. példa: ExpressRoute-áramkör ServiceKey-ének módosítása</span><span class="sxs-lookup"><span data-stu-id="d8b80-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="d8b80-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8b80-109">PARAMETERS</span></span>

### <span data-ttu-id="d8b80-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8b80-110">-AsJob</span></span>
<span data-ttu-id="d8b80-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d8b80-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b80-112">-DefaultProfile</span></span>
<span data-ttu-id="d8b80-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8b80-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b80-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d8b80-115">A parancsmag által módosított **ExpressRouteCircuit-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8b80-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d8b80-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b80-116">CommonParameters</span></span>
<span data-ttu-id="d8b80-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b80-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b80-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b80-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b80-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8b80-119">INPUTS</span></span>

### <span data-ttu-id="d8b80-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d8b80-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8b80-121">OUTPUTS</span></span>

### <span data-ttu-id="d8b80-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d8b80-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8b80-123">NOTES</span></span>

## <span data-ttu-id="d8b80-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8b80-124">RELATED LINKS</span></span>

[<span data-ttu-id="d8b80-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d8b80-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="d8b80-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="d8b80-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b80-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
