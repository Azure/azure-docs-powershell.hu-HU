---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195331"
---
# <span data-ttu-id="8a02b-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="8a02b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a02b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a02b-103">Módosítja egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="8a02b-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8a02b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a02b-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a02b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a02b-105">DESCRIPTION</span></span>
<span data-ttu-id="8a02b-106">A **set-AzExpressRouteCircuit** parancsmag a módosított ExpressRoute-áramkört az Azure-ra menti.</span><span class="sxs-lookup"><span data-stu-id="8a02b-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="8a02b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8a02b-107">EXAMPLES</span></span>

### <span data-ttu-id="8a02b-108">Példa 1: ExpressRoute-áramkör ServiceKey módosítása</span><span class="sxs-lookup"><span data-stu-id="8a02b-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="8a02b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a02b-109">PARAMETERS</span></span>

### <span data-ttu-id="8a02b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a02b-110">-AsJob</span></span>
<span data-ttu-id="8a02b-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8a02b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a02b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a02b-112">-DefaultProfile</span></span>
<span data-ttu-id="8a02b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a02b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a02b-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8a02b-115">Azt a **ExpressRouteCircuit** objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="8a02b-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8a02b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a02b-116">CommonParameters</span></span>
<span data-ttu-id="8a02b-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a02b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a02b-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a02b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a02b-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a02b-119">INPUTS</span></span>

### <span data-ttu-id="8a02b-120">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8a02b-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a02b-121">OUTPUTS</span></span>

### <span data-ttu-id="8a02b-122">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8a02b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a02b-123">NOTES</span></span>

## <span data-ttu-id="8a02b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a02b-124">RELATED LINKS</span></span>

[<span data-ttu-id="8a02b-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8a02b-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="8a02b-127">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="8a02b-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a02b-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
