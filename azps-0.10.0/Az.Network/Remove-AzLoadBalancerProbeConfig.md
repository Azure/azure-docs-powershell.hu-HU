---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841134"
---
# <span data-ttu-id="7b35d-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b35d-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7b35d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b35d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b35d-103">A szonda konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7b35d-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="7b35d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b35d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b35d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b35d-105">DESCRIPTION</span></span>
<span data-ttu-id="7b35d-106">A **Remove-AzLoadBalancerProbeConfig** parancsmagja eltávolítja a szonda konfigurációját a terheléselosztó bővítményből.</span><span class="sxs-lookup"><span data-stu-id="7b35d-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="7b35d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7b35d-107">EXAMPLES</span></span>

### <span data-ttu-id="7b35d-108">1. példa: a szonda konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="7b35d-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7b35d-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7b35d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="7b35d-110">A második parancs törli a MyProbe nevű konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="7b35d-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="7b35d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b35d-111">PARAMETERS</span></span>

### <span data-ttu-id="7b35d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b35d-112">-DefaultProfile</span></span>
<span data-ttu-id="7b35d-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b35d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b35d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b35d-114">-LoadBalancer</span></span>
<span data-ttu-id="7b35d-115">Itt adhatja meg azt a terheléselosztó konfigurációt, amely a parancsmag által eltávolított szondát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7b35d-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b35d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b35d-116">-Name</span></span>
<span data-ttu-id="7b35d-117">Annak a szonda-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="7b35d-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b35d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b35d-118">CommonParameters</span></span>
<span data-ttu-id="7b35d-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b35d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b35d-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b35d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b35d-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b35d-121">INPUTS</span></span>

### <span data-ttu-id="7b35d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b35d-122">PSLoadBalancer</span></span>
<span data-ttu-id="7b35d-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7b35d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7b35d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b35d-124">OUTPUTS</span></span>

### <span data-ttu-id="7b35d-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b35d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7b35d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b35d-126">NOTES</span></span>

## <span data-ttu-id="7b35d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b35d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b35d-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b35d-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7b35d-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b35d-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7b35d-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b35d-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7b35d-131">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b35d-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7b35d-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b35d-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


