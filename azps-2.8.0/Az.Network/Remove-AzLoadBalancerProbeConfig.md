---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6a1e5f4de5ec98030cc9bd3300d9e9fd447f6f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837101"
---
# <span data-ttu-id="9332f-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9332f-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9332f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9332f-102">SYNOPSIS</span></span>
<span data-ttu-id="9332f-103">A szonda konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="9332f-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="9332f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9332f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9332f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9332f-105">DESCRIPTION</span></span>
<span data-ttu-id="9332f-106">A **Remove-AzLoadBalancerProbeConfig** parancsmagja eltávolítja a szonda konfigurációját a terheléselosztó bővítményből.</span><span class="sxs-lookup"><span data-stu-id="9332f-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="9332f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9332f-107">EXAMPLES</span></span>

### <span data-ttu-id="9332f-108">1. példa: a szonda konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="9332f-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9332f-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9332f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="9332f-110">A második parancs törli a MyProbe nevű konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="9332f-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="9332f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9332f-111">PARAMETERS</span></span>

### <span data-ttu-id="9332f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9332f-112">-DefaultProfile</span></span>
<span data-ttu-id="9332f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9332f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9332f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9332f-114">-LoadBalancer</span></span>
<span data-ttu-id="9332f-115">Itt adhatja meg azt a terheléselosztó konfigurációt, amely a parancsmag által eltávolított szondát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9332f-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9332f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9332f-116">-Name</span></span>
<span data-ttu-id="9332f-117">Annak a szonda-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9332f-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9332f-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9332f-118">-Confirm</span></span>
<span data-ttu-id="9332f-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9332f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9332f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9332f-120">-WhatIf</span></span>
<span data-ttu-id="9332f-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9332f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9332f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9332f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9332f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9332f-123">CommonParameters</span></span>
<span data-ttu-id="9332f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9332f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9332f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9332f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9332f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9332f-126">INPUTS</span></span>

### <span data-ttu-id="9332f-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9332f-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9332f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9332f-128">OUTPUTS</span></span>

### <span data-ttu-id="9332f-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9332f-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9332f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9332f-130">NOTES</span></span>

## <span data-ttu-id="9332f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9332f-131">RELATED LINKS</span></span>

[<span data-ttu-id="9332f-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9332f-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9332f-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9332f-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9332f-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9332f-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9332f-135">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9332f-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9332f-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9332f-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


