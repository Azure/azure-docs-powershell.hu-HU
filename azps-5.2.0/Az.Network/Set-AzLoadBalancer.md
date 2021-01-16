---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367371"
---
# <span data-ttu-id="397ec-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="397ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="397ec-102">SYNOPSIS</span></span>
<span data-ttu-id="397ec-103">Frissíti a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="397ec-103">Updates a load balancer.</span></span>

## <span data-ttu-id="397ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="397ec-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="397ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="397ec-105">DESCRIPTION</span></span>
<span data-ttu-id="397ec-106">A **Set-AzLoadBalancer** parancsmag frissíti a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="397ec-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="397ec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="397ec-107">EXAMPLES</span></span>

### <span data-ttu-id="397ec-108">1. példa: Terheléselosztás módosítása</span><span class="sxs-lookup"><span data-stu-id="397ec-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="397ec-109">Az első parancs lejátsa a terheléselosztási terheléselosztás nevét, majd tárolja azt a $slb változóban.</span><span class="sxs-lookup"><span data-stu-id="397ec-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="397ec-110">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az Add-AzLoadBalancerInboundNatRuleConfig szolgáltatónak, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="397ec-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="397ec-111">A harmadik parancs átadja a terheléselosztást a **Set-AzLoadBalancernek,** amely frissíti és menti a terheléselosztás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="397ec-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="397ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="397ec-112">PARAMETERS</span></span>

### <span data-ttu-id="397ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="397ec-113">-AsJob</span></span>
<span data-ttu-id="397ec-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="397ec-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="397ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397ec-115">-DefaultProfile</span></span>
<span data-ttu-id="397ec-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="397ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="397ec-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-117">-LoadBalancer</span></span>
<span data-ttu-id="397ec-118">Egy terheléselosztási objektumot ad meg, amely azt az állapotot jelzi, amelyben a terheléselosztást be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="397ec-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="397ec-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="397ec-119">-Confirm</span></span>
<span data-ttu-id="397ec-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="397ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="397ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="397ec-121">-WhatIf</span></span>
<span data-ttu-id="397ec-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="397ec-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="397ec-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="397ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="397ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397ec-124">CommonParameters</span></span>
<span data-ttu-id="397ec-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397ec-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397ec-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="397ec-127">INPUTS</span></span>

### <span data-ttu-id="397ec-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="397ec-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="397ec-129">OUTPUTS</span></span>

### <span data-ttu-id="397ec-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="397ec-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="397ec-131">NOTES</span></span>

## <span data-ttu-id="397ec-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="397ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="397ec-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="397ec-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="397ec-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="397ec-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


