---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181520"
---
# <span data-ttu-id="40d44-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="40d44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40d44-102">SYNOPSIS</span></span>
<span data-ttu-id="40d44-103">A terheléselosztó frissítése</span><span class="sxs-lookup"><span data-stu-id="40d44-103">Updates a load balancer.</span></span>

## <span data-ttu-id="40d44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40d44-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40d44-105">DESCRIPTION</span></span>
<span data-ttu-id="40d44-106">A **set-AzLoadBalancer** parancsmag kiegyenlítő terheléselosztást frissít.</span><span class="sxs-lookup"><span data-stu-id="40d44-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="40d44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40d44-107">EXAMPLES</span></span>

### <span data-ttu-id="40d44-108">Példa 1: terheléselosztó módosítása</span><span class="sxs-lookup"><span data-stu-id="40d44-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="40d44-109">Az első parancs megkapja a NRPLB nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40d44-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="40d44-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerInboundNatRuleConfig-hoz, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="40d44-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="40d44-111">A harmadik parancs átadja a terheléselosztó beállítását a **set-AzLoadBalancer** , amely frissíti a terheléselosztó konfigurációját, és menti azt.</span><span class="sxs-lookup"><span data-stu-id="40d44-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="40d44-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40d44-112">PARAMETERS</span></span>

### <span data-ttu-id="40d44-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40d44-113">-AsJob</span></span>
<span data-ttu-id="40d44-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="40d44-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40d44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d44-115">-DefaultProfile</span></span>
<span data-ttu-id="40d44-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40d44-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d44-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-117">-LoadBalancer</span></span>
<span data-ttu-id="40d44-118">Egy olyan terheléselosztó objektumot ad meg, amely azt az állapotot képviseli, amelyre a terheléselosztót be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="40d44-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="40d44-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40d44-119">-Confirm</span></span>
<span data-ttu-id="40d44-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40d44-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d44-121">-WhatIf</span></span>
<span data-ttu-id="40d44-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40d44-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40d44-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40d44-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d44-124">CommonParameters</span></span>
<span data-ttu-id="40d44-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40d44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d44-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d44-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d44-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d44-127">INPUTS</span></span>

### <span data-ttu-id="40d44-128">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="40d44-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d44-129">OUTPUTS</span></span>

### <span data-ttu-id="40d44-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="40d44-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40d44-131">NOTES</span></span>

## <span data-ttu-id="40d44-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40d44-132">RELATED LINKS</span></span>

[<span data-ttu-id="40d44-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="40d44-134">Új – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="40d44-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40d44-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


