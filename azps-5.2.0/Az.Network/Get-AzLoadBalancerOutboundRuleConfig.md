---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345486"
---
# <span data-ttu-id="416e2-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="416e2-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="416e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="416e2-102">SYNOPSIS</span></span>
<span data-ttu-id="416e2-103">Kimenő szabálykonfigurációt kap a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="416e2-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="416e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="416e2-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="416e2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="416e2-105">DESCRIPTION</span></span>
<span data-ttu-id="416e2-106">A **Get-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt vagy a kimenő szabálykonfigurációk listáját kapja egy terheléselegyenlőben.</span><span class="sxs-lookup"><span data-stu-id="416e2-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="416e2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="416e2-107">EXAMPLES</span></span>

### <span data-ttu-id="416e2-108">1. példa: Kimenő szabály konfigurálása terheléselosztásban</span><span class="sxs-lookup"><span data-stu-id="416e2-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="416e2-109">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="416e2-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="416e2-110">A második parancs a MyRule nevű kimenő szabálykonfigurációt kapja hozzá a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="416e2-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="416e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="416e2-111">PARAMETERS</span></span>

### <span data-ttu-id="416e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="416e2-112">-DefaultProfile</span></span>
<span data-ttu-id="416e2-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="416e2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="416e2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="416e2-114">-LoadBalancer</span></span>
<span data-ttu-id="416e2-115">A terheléselosztási erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="416e2-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="416e2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="416e2-116">-Name</span></span>
<span data-ttu-id="416e2-117">A kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="416e2-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="416e2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="416e2-118">CommonParameters</span></span>
<span data-ttu-id="416e2-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="416e2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="416e2-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="416e2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="416e2-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="416e2-121">INPUTS</span></span>

### <span data-ttu-id="416e2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="416e2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="416e2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="416e2-123">OUTPUTS</span></span>

### <span data-ttu-id="416e2-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="416e2-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="416e2-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="416e2-125">NOTES</span></span>

## <span data-ttu-id="416e2-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="416e2-126">RELATED LINKS</span></span>

[<span data-ttu-id="416e2-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="416e2-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="416e2-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="416e2-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="416e2-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="416e2-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="416e2-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="416e2-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
