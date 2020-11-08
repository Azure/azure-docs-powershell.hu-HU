---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186219"
---
# <span data-ttu-id="84c10-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c10-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="84c10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84c10-102">SYNOPSIS</span></span>
<span data-ttu-id="84c10-103">Kinyeri a szabály konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="84c10-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="84c10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84c10-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84c10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84c10-105">DESCRIPTION</span></span>
<span data-ttu-id="84c10-106">A **Get-AzLoadBalancerRuleConfig** parancsmag egy vagy több szabály-konfigurációt kap a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="84c10-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="84c10-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84c10-107">EXAMPLES</span></span>

### <span data-ttu-id="84c10-108">Példa 1: terheléselosztó szabály-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="84c10-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="84c10-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="84c10-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="84c10-110">A második parancs beolvassa a MyLBrulename nevű társított szabály konfigurációját a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="84c10-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="84c10-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84c10-111">PARAMETERS</span></span>

### <span data-ttu-id="84c10-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c10-112">-DefaultProfile</span></span>
<span data-ttu-id="84c10-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84c10-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c10-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84c10-114">-LoadBalancer</span></span>
<span data-ttu-id="84c10-115">A beolvasás szabály konfigurációjával társított terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="84c10-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="84c10-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84c10-116">-Name</span></span>
<span data-ttu-id="84c10-117">A beolvasott szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84c10-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="84c10-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c10-118">CommonParameters</span></span>
<span data-ttu-id="84c10-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84c10-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c10-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84c10-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c10-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84c10-121">INPUTS</span></span>

### <span data-ttu-id="84c10-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84c10-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="84c10-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84c10-123">OUTPUTS</span></span>

### <span data-ttu-id="84c10-124">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="84c10-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="84c10-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84c10-125">NOTES</span></span>

## <span data-ttu-id="84c10-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84c10-126">RELATED LINKS</span></span>

[<span data-ttu-id="84c10-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c10-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="84c10-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84c10-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="84c10-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c10-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="84c10-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84c10-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


