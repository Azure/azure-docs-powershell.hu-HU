---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2cafba2d579a37db45f12c5e3dd1746f799bfe21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921017"
---
# <span data-ttu-id="44580-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44580-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="44580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44580-102">SYNOPSIS</span></span>
<span data-ttu-id="44580-103">Előlapi IP-konfigurációt kap a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="44580-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="44580-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44580-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44580-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44580-105">DESCRIPTION</span></span>
<span data-ttu-id="44580-106">A **Get-AzLoadBalancerFrontendIpConfig** parancsmag egy előlapi IP-konfigurációt vagy az előlapi IP-konfigurációk listáját kapja egy terheléselegyenítőben.</span><span class="sxs-lookup"><span data-stu-id="44580-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="44580-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44580-107">EXAMPLES</span></span>

### <span data-ttu-id="44580-108">1. példa: Előlapi IP-konfiguráció beállítása terheléselosztásban</span><span class="sxs-lookup"><span data-stu-id="44580-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="44580-109">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="44580-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="44580-110">A második parancs az adott terheléselosztáshoz társított előlapi IP-konfigurációt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44580-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="44580-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44580-111">PARAMETERS</span></span>

### <span data-ttu-id="44580-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44580-112">-DefaultProfile</span></span>
<span data-ttu-id="44580-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44580-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44580-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44580-114">-LoadBalancer</span></span>
<span data-ttu-id="44580-115">Az előlapi IP-konfigurációhoz társított terheléselosztást határozza meg.</span><span class="sxs-lookup"><span data-stu-id="44580-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="44580-116">-Name</span><span class="sxs-lookup"><span data-stu-id="44580-116">-Name</span></span>
<span data-ttu-id="44580-117">Annak a terheléselosztásnak a nevét adja meg, amely az előlapi IP-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="44580-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="44580-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44580-118">CommonParameters</span></span>
<span data-ttu-id="44580-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44580-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44580-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44580-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44580-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44580-121">INPUTS</span></span>

### <span data-ttu-id="44580-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44580-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="44580-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44580-123">OUTPUTS</span></span>

### <span data-ttu-id="44580-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="44580-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="44580-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44580-125">NOTES</span></span>

## <span data-ttu-id="44580-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44580-126">RELATED LINKS</span></span>

[<span data-ttu-id="44580-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44580-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="44580-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44580-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="44580-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44580-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="44580-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44580-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="44580-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44580-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


