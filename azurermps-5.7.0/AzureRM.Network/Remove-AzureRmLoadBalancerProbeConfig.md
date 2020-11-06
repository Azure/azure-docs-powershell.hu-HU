---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9840476e64c78293b747f96d1a689a3ce5099bff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493097"
---
# <span data-ttu-id="7a6c9-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7a6c9-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7a6c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6c9-103">A szonda konfigurációjának eltávolítása a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a6c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a6c9-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a6c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6c9-106">A **Remove-AzureRmLoadBalancerProbeConfig** parancsmagja eltávolítja a szonda konfigurációját a terheléselosztó bővítményből.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="7a6c9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a6c9-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6c9-108">1. példa: a szonda konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="7a6c9-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7a6c9-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="7a6c9-110">A második parancs törli a MyProbe nevű konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="7a6c9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a6c9-111">PARAMETERS</span></span>

### <span data-ttu-id="7a6c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6c9-112">-DefaultProfile</span></span>
<span data-ttu-id="7a6c9-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a6c9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a6c9-114">-LoadBalancer</span></span>
<span data-ttu-id="7a6c9-115">Itt adhatja meg azt a terheléselosztó konfigurációt, amely a parancsmag által eltávolított szondát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a6c9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a6c9-116">-Name</span></span>
<span data-ttu-id="7a6c9-117">Annak a szonda-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="7a6c9-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a6c9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6c9-118">CommonParameters</span></span>
<span data-ttu-id="7a6c9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a6c9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6c9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6c9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6c9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a6c9-121">INPUTS</span></span>

### <span data-ttu-id="7a6c9-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a6c9-122">PSLoadBalancer</span></span>
<span data-ttu-id="7a6c9-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7a6c9-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7a6c9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a6c9-124">OUTPUTS</span></span>

### <span data-ttu-id="7a6c9-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a6c9-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7a6c9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a6c9-126">NOTES</span></span>

## <span data-ttu-id="7a6c9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a6c9-127">RELATED LINKS</span></span>

[<span data-ttu-id="7a6c9-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7a6c9-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7a6c9-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a6c9-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="7a6c9-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7a6c9-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7a6c9-131">Új – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7a6c9-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7a6c9-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7a6c9-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


