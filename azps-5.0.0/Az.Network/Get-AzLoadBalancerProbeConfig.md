---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186223"
---
# <span data-ttu-id="7c98a-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c98a-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7c98a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c98a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c98a-103">Kinyeri a szonda konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="7c98a-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="7c98a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c98a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c98a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c98a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c98a-106">A **Get-AzLoadBalancerProbeConfig** parancsmag egy vagy több szonda-konfigurációt kap a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="7c98a-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="7c98a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c98a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c98a-108">1. példa: a terheléselosztó szonda-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="7c98a-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="7c98a-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="7c98a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="7c98a-110">A második parancs beolvassa a MyProbe nevű társított szonda-konfigurációt a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="7c98a-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="7c98a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c98a-111">PARAMETERS</span></span>

### <span data-ttu-id="7c98a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c98a-112">-DefaultProfile</span></span>
<span data-ttu-id="7c98a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c98a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c98a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c98a-114">-LoadBalancer</span></span>
<span data-ttu-id="7c98a-115">A szonda konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c98a-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="7c98a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c98a-116">-Name</span></span>
<span data-ttu-id="7c98a-117">A beszerzéshez használandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c98a-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="7c98a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c98a-118">CommonParameters</span></span>
<span data-ttu-id="7c98a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c98a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c98a-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c98a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c98a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c98a-121">INPUTS</span></span>

### <span data-ttu-id="7c98a-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c98a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7c98a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c98a-123">OUTPUTS</span></span>

### <span data-ttu-id="7c98a-124">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="7c98a-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="7c98a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c98a-125">NOTES</span></span>

## <span data-ttu-id="7c98a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c98a-126">RELATED LINKS</span></span>

[<span data-ttu-id="7c98a-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c98a-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7c98a-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c98a-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7c98a-129">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c98a-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7c98a-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c98a-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7c98a-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c98a-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


