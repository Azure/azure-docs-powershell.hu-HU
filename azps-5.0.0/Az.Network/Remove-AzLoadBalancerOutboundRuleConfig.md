---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188242"
---
# <span data-ttu-id="d41ca-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d41ca-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="d41ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d41ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d41ca-103">Kimenő szabály konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d41ca-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="d41ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d41ca-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d41ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d41ca-105">DESCRIPTION</span></span>
<span data-ttu-id="d41ca-106">A **Remove-AzLoadBalancerOutboundRuleConfig** parancsmag egy kimenő szabály konfigurációját az Azure terheléselosztó szolgáltatásból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="d41ca-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="d41ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d41ca-107">EXAMPLES</span></span>

### <span data-ttu-id="d41ca-108">1. példa: egy kimenő szabály törlése Azure terheléselosztó szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="d41ca-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="d41ca-109">Az első parancs megkapja az eltávolítani kívánt Kimenő szabály konfigurációjának megfelelő terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d41ca-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="d41ca-110">A második parancs eltávolítja a kapcsolódó Kimenő szabály konfigurációját a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d41ca-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="d41ca-111">A harmadik parancs frissíti a terheléselosztó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="d41ca-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="d41ca-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d41ca-112">PARAMETERS</span></span>

### <span data-ttu-id="d41ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41ca-113">-DefaultProfile</span></span>
<span data-ttu-id="d41ca-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d41ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d41ca-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d41ca-115">-LoadBalancer</span></span>
<span data-ttu-id="d41ca-116">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="d41ca-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="d41ca-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d41ca-117">-Name</span></span>
<span data-ttu-id="d41ca-118">A Kimenő szabály neve</span><span class="sxs-lookup"><span data-stu-id="d41ca-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="d41ca-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d41ca-119">-Confirm</span></span>
<span data-ttu-id="d41ca-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d41ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d41ca-121">-WhatIf</span></span>
<span data-ttu-id="d41ca-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d41ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d41ca-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d41ca-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41ca-124">CommonParameters</span></span>
<span data-ttu-id="d41ca-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d41ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41ca-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41ca-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41ca-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d41ca-127">INPUTS</span></span>

### <span data-ttu-id="d41ca-128">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d41ca-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d41ca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d41ca-129">OUTPUTS</span></span>

### <span data-ttu-id="d41ca-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d41ca-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d41ca-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d41ca-131">NOTES</span></span>

## <span data-ttu-id="d41ca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d41ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="d41ca-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d41ca-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d41ca-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d41ca-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d41ca-135">Új – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d41ca-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d41ca-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d41ca-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)