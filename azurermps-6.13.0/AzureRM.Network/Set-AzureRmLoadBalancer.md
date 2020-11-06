---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 5090d97157e608b2c3f6ef52d6eafa932ae4be50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499475"
---
# <span data-ttu-id="c9c93-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="c9c93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9c93-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c93-103">A terheléselosztó cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="c9c93-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9c93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9c93-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9c93-105">DESCRIPTION</span></span>
<span data-ttu-id="c9c93-106">A **set-AzureRmLoadBalancer** parancsmag az Azure terheléselosztó cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="c9c93-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="c9c93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9c93-107">EXAMPLES</span></span>

### <span data-ttu-id="c9c93-108">Példa 1: terheléselosztó módosítása</span><span class="sxs-lookup"><span data-stu-id="c9c93-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c9c93-109">Az első parancs megkapja a NRPLB nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9c93-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c9c93-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzureRmLoadBalancerInboundNatRuleConfig-hoz, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c9c93-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="c9c93-111">A harmadik parancs átadja a terheléselosztó beállítását a **set-AzureRmLoadBalancer** , amely frissíti a terheléselosztó konfigurációját, és menti azt.</span><span class="sxs-lookup"><span data-stu-id="c9c93-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="c9c93-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9c93-112">PARAMETERS</span></span>

### <span data-ttu-id="c9c93-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9c93-113">-AsJob</span></span>
<span data-ttu-id="c9c93-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c9c93-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9c93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c93-115">-DefaultProfile</span></span>
<span data-ttu-id="c9c93-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9c93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9c93-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-117">-LoadBalancer</span></span>
<span data-ttu-id="c9c93-118">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9c93-118">Specifies a load balancer.</span></span>
<span data-ttu-id="c9c93-119">Ez a parancsmag a paraméter által megadott terheléselosztó cél állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c9c93-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c93-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9c93-120">-Confirm</span></span>
<span data-ttu-id="c9c93-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9c93-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c93-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c93-122">-WhatIf</span></span>
<span data-ttu-id="c9c93-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9c93-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9c93-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9c93-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c93-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c93-125">CommonParameters</span></span>
<span data-ttu-id="c9c93-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9c93-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c93-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c93-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c93-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c93-128">INPUTS</span></span>

### <span data-ttu-id="c9c93-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c9c93-130">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9c93-130">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="c9c93-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c93-131">OUTPUTS</span></span>

### <span data-ttu-id="c9c93-132">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-132">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c9c93-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9c93-133">NOTES</span></span>

## <span data-ttu-id="c9c93-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9c93-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9c93-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c9c93-136">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-136">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="c9c93-137">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9c93-137">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


