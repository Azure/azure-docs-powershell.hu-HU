---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: d16e0579224907885a2239aa0669ae865ed19dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837777"
---
# <span data-ttu-id="c2895-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="c2895-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2895-102">SYNOPSIS</span></span>
<span data-ttu-id="c2895-103">A terheléselosztó frissítése</span><span class="sxs-lookup"><span data-stu-id="c2895-103">Updates a load balancer.</span></span>

## <span data-ttu-id="c2895-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2895-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2895-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2895-105">DESCRIPTION</span></span>
<span data-ttu-id="c2895-106">A **set-AzLoadBalancer** parancsmag kiegyenlítő terheléselosztást frissít.</span><span class="sxs-lookup"><span data-stu-id="c2895-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="c2895-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c2895-107">EXAMPLES</span></span>

### <span data-ttu-id="c2895-108">Példa 1: terheléselosztó módosítása</span><span class="sxs-lookup"><span data-stu-id="c2895-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="c2895-109">Az első parancs megkapja a NRPLB nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c2895-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c2895-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerInboundNatRuleConfig-hoz, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c2895-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="c2895-111">A harmadik parancs átadja a terheléselosztó beállítását a **set-AzLoadBalancer** , amely frissíti a terheléselosztó konfigurációját, és menti azt.</span><span class="sxs-lookup"><span data-stu-id="c2895-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="c2895-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2895-112">PARAMETERS</span></span>

### <span data-ttu-id="c2895-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2895-113">-AsJob</span></span>
<span data-ttu-id="c2895-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2895-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2895-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2895-115">-DefaultProfile</span></span>
<span data-ttu-id="c2895-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2895-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2895-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-117">-LoadBalancer</span></span>
<span data-ttu-id="c2895-118">Egy olyan terheléselosztó objektumot ad meg, amely azt az állapotot képviseli, amelyre a terheléselosztót be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c2895-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="c2895-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2895-119">-Confirm</span></span>
<span data-ttu-id="c2895-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2895-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2895-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2895-121">-WhatIf</span></span>
<span data-ttu-id="c2895-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2895-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2895-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2895-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2895-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2895-124">CommonParameters</span></span>
<span data-ttu-id="c2895-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2895-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2895-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2895-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2895-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2895-127">INPUTS</span></span>

### <span data-ttu-id="c2895-128">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c2895-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2895-129">OUTPUTS</span></span>

### <span data-ttu-id="c2895-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c2895-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2895-131">NOTES</span></span>

## <span data-ttu-id="c2895-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2895-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2895-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c2895-134">Új – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="c2895-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2895-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


