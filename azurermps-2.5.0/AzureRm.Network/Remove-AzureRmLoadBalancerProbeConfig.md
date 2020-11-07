---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: bed9eebb8812c0bd75eb19c3e8666d6a3b418a13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850626"
---
# <span data-ttu-id="fa917-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fa917-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="fa917-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa917-102">SYNOPSIS</span></span>
<span data-ttu-id="fa917-103">A szonda konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="fa917-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa917-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa917-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa917-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa917-105">DESCRIPTION</span></span>
<span data-ttu-id="fa917-106">A **Remove-AzureRmLoadBalancerProbeConfig** parancsmagja eltávolítja a szonda konfigurációját a terheléselosztó bővítményből.</span><span class="sxs-lookup"><span data-stu-id="fa917-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="fa917-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fa917-107">EXAMPLES</span></span>

### <span data-ttu-id="fa917-108">1. példa: a szonda konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="fa917-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="fa917-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fa917-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="fa917-110">A második parancs törli a MyProbe nevű konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="fa917-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="fa917-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa917-111">PARAMETERS</span></span>

### <span data-ttu-id="fa917-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa917-112">-DefaultProfile</span></span>
<span data-ttu-id="fa917-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa917-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa917-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa917-114">-LoadBalancer</span></span>
<span data-ttu-id="fa917-115">Itt adhatja meg azt a terheléselosztó konfigurációt, amely a parancsmag által eltávolított szondát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fa917-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fa917-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa917-116">-Name</span></span>
<span data-ttu-id="fa917-117">Annak a szonda-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="fa917-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa917-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa917-118">CommonParameters</span></span>
<span data-ttu-id="fa917-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa917-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa917-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa917-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa917-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa917-121">INPUTS</span></span>

### <span data-ttu-id="fa917-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa917-122">PSLoadBalancer</span></span>
<span data-ttu-id="fa917-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fa917-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fa917-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa917-124">OUTPUTS</span></span>

### <span data-ttu-id="fa917-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa917-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fa917-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa917-126">NOTES</span></span>

## <span data-ttu-id="fa917-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa917-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa917-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fa917-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="fa917-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa917-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fa917-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fa917-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="fa917-131">Új – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fa917-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="fa917-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fa917-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


