---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: b608a8fe62f7316116409d4174ea01603b928ae2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924585"
---
# <span data-ttu-id="c2a50-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="c2a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a50-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a50-103">Frissíti a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="c2a50-103">Updates a load balancer.</span></span>

## <span data-ttu-id="c2a50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2a50-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a50-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2a50-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a50-106">A **Set-AzLoadBalancer** parancsmag frissíti a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="c2a50-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="c2a50-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2a50-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a50-108">1. példa: Terheléselosztás módosítása</span><span class="sxs-lookup"><span data-stu-id="c2a50-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="c2a50-109">Az első parancs lekérte a terheléselosztási NRPLB nevet, majd tárolja azt a $slb változóban.</span><span class="sxs-lookup"><span data-stu-id="c2a50-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c2a50-110">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az Add-AzLoadBalancerInboundNatRuleConfig szolgáltatónak, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c2a50-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="c2a50-111">A harmadik parancs átadja a terheléselosztást a **Set-AzLoadBalancernek,** amely frissíti és menti a terheléselosztás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c2a50-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="c2a50-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a50-112">PARAMETERS</span></span>

### <span data-ttu-id="c2a50-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2a50-113">-AsJob</span></span>
<span data-ttu-id="c2a50-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2a50-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2a50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a50-115">-DefaultProfile</span></span>
<span data-ttu-id="c2a50-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2a50-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2a50-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-117">-LoadBalancer</span></span>
<span data-ttu-id="c2a50-118">Egy terheléselosztási objektumot ad meg, amely azt az állapotot jelzi, amelyben a terheléselosztást be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c2a50-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="c2a50-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2a50-119">-Confirm</span></span>
<span data-ttu-id="c2a50-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2a50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a50-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a50-121">-WhatIf</span></span>
<span data-ttu-id="c2a50-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c2a50-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2a50-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2a50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a50-124">CommonParameters</span></span>
<span data-ttu-id="c2a50-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a50-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a50-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a50-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2a50-127">INPUTS</span></span>

### <span data-ttu-id="c2a50-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c2a50-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2a50-129">OUTPUTS</span></span>

### <span data-ttu-id="c2a50-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c2a50-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2a50-131">NOTES</span></span>

## <span data-ttu-id="c2a50-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2a50-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2a50-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c2a50-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="c2a50-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2a50-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


