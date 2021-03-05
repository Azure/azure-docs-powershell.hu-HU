---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 43c3b4d17d024eaae06c7d7f891dfd2ea3e08aa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006454"
---
# <span data-ttu-id="cbfd7-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbfd7-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="cbfd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbfd7-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfd7-103">Konfigurációt kap a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="cbfd7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbfd7-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbfd7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbfd7-105">DESCRIPTION</span></span>
<span data-ttu-id="cbfd7-106">A **Get-AzLoadBalancerProbeConfig** parancsmag egy vagy több konfigurációt kap a terheléselegyenlők számára.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="cbfd7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbfd7-107">EXAMPLES</span></span>

### <span data-ttu-id="cbfd7-108">1. példa: Terheléselosztás konfigurációjának lekérte</span><span class="sxs-lookup"><span data-stu-id="cbfd7-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="cbfd7-109">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="cbfd7-110">A második parancs lekérte a MyProbe nevű konfigurációs konfigurációt a rendszer terheléselosztási $slb.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="cbfd7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbfd7-111">PARAMETERS</span></span>

### <span data-ttu-id="cbfd7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfd7-112">-DefaultProfile</span></span>
<span data-ttu-id="cbfd7-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbfd7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbfd7-114">-LoadBalancer</span></span>
<span data-ttu-id="cbfd7-115">A lekért konfigurációhoz társított terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="cbfd7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cbfd7-116">-Name</span></span>
<span data-ttu-id="cbfd7-117">A lekért konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="cbfd7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfd7-118">CommonParameters</span></span>
<span data-ttu-id="cbfd7-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbfd7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfd7-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbfd7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfd7-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbfd7-121">INPUTS</span></span>

### <span data-ttu-id="cbfd7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbfd7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cbfd7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbfd7-123">OUTPUTS</span></span>

### <span data-ttu-id="cbfd7-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="cbfd7-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="cbfd7-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbfd7-125">NOTES</span></span>

## <span data-ttu-id="cbfd7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbfd7-126">RELATED LINKS</span></span>

[<span data-ttu-id="cbfd7-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbfd7-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cbfd7-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbfd7-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="cbfd7-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbfd7-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cbfd7-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbfd7-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cbfd7-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbfd7-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


