---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188108"
---
# <span data-ttu-id="7902b-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7902b-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7902b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7902b-102">SYNOPSIS</span></span>
<span data-ttu-id="7902b-103">A szonda konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7902b-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="7902b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7902b-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7902b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7902b-105">DESCRIPTION</span></span>
<span data-ttu-id="7902b-106">A **Remove-AzLoadBalancerProbeConfig** parancsmagja eltávolítja a szonda konfigurációját a terheléselosztó bővítményből.</span><span class="sxs-lookup"><span data-stu-id="7902b-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="7902b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7902b-107">EXAMPLES</span></span>

### <span data-ttu-id="7902b-108">1. példa: a szonda konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="7902b-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7902b-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7902b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="7902b-110">A második parancs törli a MyProbe nevű konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="7902b-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="7902b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7902b-111">PARAMETERS</span></span>

### <span data-ttu-id="7902b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7902b-112">-DefaultProfile</span></span>
<span data-ttu-id="7902b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7902b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7902b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7902b-114">-LoadBalancer</span></span>
<span data-ttu-id="7902b-115">Itt adhatja meg azt a terheléselosztó konfigurációt, amely a parancsmag által eltávolított szondát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7902b-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7902b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7902b-116">-Name</span></span>
<span data-ttu-id="7902b-117">Annak a szonda-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="7902b-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7902b-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7902b-118">-Confirm</span></span>
<span data-ttu-id="7902b-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7902b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7902b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7902b-120">-WhatIf</span></span>
<span data-ttu-id="7902b-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7902b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7902b-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7902b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7902b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7902b-123">CommonParameters</span></span>
<span data-ttu-id="7902b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7902b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7902b-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7902b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7902b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7902b-126">INPUTS</span></span>

### <span data-ttu-id="7902b-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7902b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7902b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7902b-128">OUTPUTS</span></span>

### <span data-ttu-id="7902b-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7902b-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7902b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7902b-130">NOTES</span></span>

## <span data-ttu-id="7902b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7902b-131">RELATED LINKS</span></span>

[<span data-ttu-id="7902b-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7902b-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7902b-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7902b-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7902b-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7902b-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7902b-135">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7902b-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7902b-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7902b-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)

