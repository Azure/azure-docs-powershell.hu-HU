---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494454"
---
# <span data-ttu-id="99c4c-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="99c4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="99c4c-103">A terheléselosztó cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="99c4c-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99c4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99c4c-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99c4c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="99c4c-106">A **set-AzureRmLoadBalancer** parancsmag az Azure terheléselosztó cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="99c4c-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="99c4c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="99c4c-108">Példa 1: terheléselosztó módosítása</span><span class="sxs-lookup"><span data-stu-id="99c4c-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="99c4c-109">Az első parancs megkapja a NRPLB nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="99c4c-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="99c4c-110">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzureRmLoadBalancerInboundNatRuleConfig-hoz, amely egy NewRule nevű bejövő NAT-szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="99c4c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="99c4c-111">A harmadik parancs átadja a terheléselosztó beállítását a **set-AzureRmLoadBalancer** , amely frissíti a terheléselosztó konfigurációját, és menti azt.</span><span class="sxs-lookup"><span data-stu-id="99c4c-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="99c4c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99c4c-112">PARAMETERS</span></span>

### <span data-ttu-id="99c4c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99c4c-113">-AsJob</span></span>
<span data-ttu-id="99c4c-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99c4c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99c4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c4c-115">-DefaultProfile</span></span>
<span data-ttu-id="99c4c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99c4c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c4c-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-117">-LoadBalancer</span></span>
<span data-ttu-id="99c4c-118">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="99c4c-118">Specifies a load balancer.</span></span>
<span data-ttu-id="99c4c-119">Ez a parancsmag a paraméter által megadott terheléselosztó cél állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="99c4c-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="99c4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c4c-120">CommonParameters</span></span>
<span data-ttu-id="99c4c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99c4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c4c-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c4c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c4c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c4c-123">INPUTS</span></span>

### <span data-ttu-id="99c4c-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-124">PSLoadBalancer</span></span>
<span data-ttu-id="99c4c-125">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="99c4c-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="99c4c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c4c-126">OUTPUTS</span></span>

### <span data-ttu-id="99c4c-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99c4c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99c4c-128">NOTES</span></span>

## <span data-ttu-id="99c4c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99c4c-129">RELATED LINKS</span></span>

[<span data-ttu-id="99c4c-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="99c4c-131">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="99c4c-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c4c-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


