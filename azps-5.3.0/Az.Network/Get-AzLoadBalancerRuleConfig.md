---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380084"
---
# <span data-ttu-id="e6ebd-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6ebd-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e6ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ebd-103">A terheléselosztás szabálykonfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e6ebd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6ebd-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ebd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ebd-106">A **Get-AzLoadBalancerRuleConfig** parancsmag egy vagy több szabálykonfigurációt kap a terheléselegyenlők számára.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="e6ebd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6ebd-107">EXAMPLES</span></span>

### <span data-ttu-id="e6ebd-108">1. példa: Terheléselosztás szabálykonfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="e6ebd-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="e6ebd-109">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e6ebd-110">A második parancs a myLName nevű társított szabálykonfigurációt a rendszer terheléselosztási $slb.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="e6ebd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ebd-111">PARAMETERS</span></span>

### <span data-ttu-id="e6ebd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ebd-112">-DefaultProfile</span></span>
<span data-ttu-id="e6ebd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6ebd-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6ebd-114">-LoadBalancer</span></span>
<span data-ttu-id="e6ebd-115">Megadja a lekért szabálykonfigurációhoz társított terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ebd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e6ebd-116">-Name</span></span>
<span data-ttu-id="e6ebd-117">A lekért szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-117">Specifies the name of the rule configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ebd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ebd-118">CommonParameters</span></span>
<span data-ttu-id="e6ebd-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ebd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ebd-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6ebd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ebd-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6ebd-121">INPUTS</span></span>

### <span data-ttu-id="e6ebd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6ebd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e6ebd-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ebd-123">OUTPUTS</span></span>

### <span data-ttu-id="e6ebd-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="e6ebd-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="e6ebd-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6ebd-125">NOTES</span></span>

## <span data-ttu-id="e6ebd-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6ebd-126">RELATED LINKS</span></span>

[<span data-ttu-id="e6ebd-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6ebd-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="e6ebd-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6ebd-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e6ebd-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6ebd-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="e6ebd-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6ebd-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


