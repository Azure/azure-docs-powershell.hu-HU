---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013337"
---
# <span data-ttu-id="b68af-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b68af-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b68af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b68af-102">SYNOPSIS</span></span>
<span data-ttu-id="b68af-103">Beilleszti az előtér IP-konfigurációját egy terheléselosztó nézetben.</span><span class="sxs-lookup"><span data-stu-id="b68af-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="b68af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b68af-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b68af-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b68af-105">DESCRIPTION</span></span>
<span data-ttu-id="b68af-106">A **Get-AzLoadBalancerFrontendIpConfig** parancsmag az előtér IP-konfigurációját, illetve az előtér IP-konfigurációinak listáját a terheléselosztásban kapja.</span><span class="sxs-lookup"><span data-stu-id="b68af-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="b68af-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b68af-107">EXAMPLES</span></span>

### <span data-ttu-id="b68af-108">1. példa: az előtér IP-konfigurációjának beszerzése a terheléselosztó bővítményben</span><span class="sxs-lookup"><span data-stu-id="b68af-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="b68af-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="b68af-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b68af-110">A második parancs beilleszti az előtér-végponthoz társított IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b68af-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="b68af-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b68af-111">PARAMETERS</span></span>

### <span data-ttu-id="b68af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68af-112">-DefaultProfile</span></span>
<span data-ttu-id="b68af-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b68af-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b68af-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b68af-114">-LoadBalancer</span></span>
<span data-ttu-id="b68af-115">Annak az IP-konfigurációnak a terheléselosztását adja meg, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="b68af-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="b68af-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b68af-116">-Name</span></span>
<span data-ttu-id="b68af-117">Annak az IP-konfigurációnak a neve, amely az előtér IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b68af-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="b68af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68af-118">CommonParameters</span></span>
<span data-ttu-id="b68af-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b68af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68af-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b68af-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68af-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b68af-121">INPUTS</span></span>

### <span data-ttu-id="b68af-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b68af-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b68af-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b68af-123">OUTPUTS</span></span>

### <span data-ttu-id="b68af-124">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b68af-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b68af-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b68af-125">NOTES</span></span>

## <span data-ttu-id="b68af-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b68af-126">RELATED LINKS</span></span>

[<span data-ttu-id="b68af-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b68af-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b68af-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b68af-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b68af-129">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b68af-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b68af-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b68af-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b68af-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b68af-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


