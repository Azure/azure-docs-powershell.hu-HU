---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161090"
---
# <span data-ttu-id="0f8bd-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f8bd-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="0f8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8bd-103">Kimenő szabálykonfigurációt kap a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="0f8bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f8bd-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f8bd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="0f8bd-106">A **Get-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt vagy a kimenő szabálykonfigurációk listáját kapja egy terheléselegyenlőben.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="0f8bd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f8bd-107">EXAMPLES</span></span>

### <span data-ttu-id="0f8bd-108">1. példa: Kimenő szabály konfigurálása terheléselosztásban</span><span class="sxs-lookup"><span data-stu-id="0f8bd-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="0f8bd-109">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0f8bd-110">A második parancs a MyRule nevű kimenő szabálykonfigurációt kapja hozzá a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="0f8bd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f8bd-111">PARAMETERS</span></span>

### <span data-ttu-id="0f8bd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8bd-112">-DefaultProfile</span></span>
<span data-ttu-id="0f8bd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f8bd-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f8bd-114">-LoadBalancer</span></span>
<span data-ttu-id="0f8bd-115">A terheléselosztási erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="0f8bd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0f8bd-116">-Name</span></span>
<span data-ttu-id="0f8bd-117">A kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="0f8bd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8bd-118">CommonParameters</span></span>
<span data-ttu-id="0f8bd-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8bd-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f8bd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8bd-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f8bd-121">INPUTS</span></span>

### <span data-ttu-id="0f8bd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f8bd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f8bd-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f8bd-123">OUTPUTS</span></span>

### <span data-ttu-id="0f8bd-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="0f8bd-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="0f8bd-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f8bd-125">NOTES</span></span>

## <span data-ttu-id="0f8bd-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f8bd-126">RELATED LINKS</span></span>

[<span data-ttu-id="0f8bd-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f8bd-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0f8bd-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f8bd-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0f8bd-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f8bd-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0f8bd-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f8bd-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
