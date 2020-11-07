---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843642"
---
# <span data-ttu-id="27864-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="27864-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27864-102">SYNOPSIS</span></span>
<span data-ttu-id="27864-103">A terheléselosztó cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="27864-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="27864-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27864-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27864-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27864-105">DESCRIPTION</span></span>
<span data-ttu-id="27864-106">A **set-AzLoadBalancer** parancsmag az Azure terheléselosztó cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="27864-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="27864-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27864-107">EXAMPLES</span></span>

### <span data-ttu-id="27864-108">Példa 1: terheléselosztó módosítása</span><span class="sxs-lookup"><span data-stu-id="27864-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="27864-109">Az első parancs megkapja a NRPLB nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="27864-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="27864-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerInboundNatRuleConfig-hoz, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="27864-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="27864-111">A harmadik parancs átadja a terheléselosztó beállítását a **set-AzLoadBalancer** , amely frissíti a terheléselosztó konfigurációját, és menti azt.</span><span class="sxs-lookup"><span data-stu-id="27864-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="27864-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27864-112">PARAMETERS</span></span>

### <span data-ttu-id="27864-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27864-113">-AsJob</span></span>
<span data-ttu-id="27864-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="27864-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27864-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27864-115">-DefaultProfile</span></span>
<span data-ttu-id="27864-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27864-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27864-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-117">-LoadBalancer</span></span>
<span data-ttu-id="27864-118">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="27864-118">Specifies a load balancer.</span></span>
<span data-ttu-id="27864-119">Ez a parancsmag a paraméter által megadott terheléselosztó cél állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="27864-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27864-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27864-120">CommonParameters</span></span>
<span data-ttu-id="27864-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27864-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27864-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27864-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27864-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27864-123">INPUTS</span></span>

### <span data-ttu-id="27864-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-124">PSLoadBalancer</span></span>
<span data-ttu-id="27864-125">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="27864-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="27864-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27864-126">OUTPUTS</span></span>

### <span data-ttu-id="27864-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27864-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27864-128">NOTES</span></span>

## <span data-ttu-id="27864-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27864-129">RELATED LINKS</span></span>

[<span data-ttu-id="27864-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="27864-131">Új – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="27864-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27864-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


