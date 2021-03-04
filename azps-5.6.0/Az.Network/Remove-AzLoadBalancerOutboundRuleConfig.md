---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 5652615cf8072e4a448f2fe6c6d4b3fd784cc330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941602"
---
# <span data-ttu-id="cacea-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cacea-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="cacea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cacea-102">SYNOPSIS</span></span>
<span data-ttu-id="cacea-103">A kimenő szabálykonfiguráció eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="cacea-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="cacea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cacea-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cacea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cacea-105">DESCRIPTION</span></span>
<span data-ttu-id="cacea-106">A **Remove-AzLoadBalancerOutboundRuleConfig** parancsmag eltávolít egy kimenő szabálykonfigurációt egy Azure-terheléselegyenlőből.</span><span class="sxs-lookup"><span data-stu-id="cacea-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="cacea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cacea-107">EXAMPLES</span></span>

### <span data-ttu-id="cacea-108">1. példa: Kimenő szabály törlése az Azure terheléselosztási szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="cacea-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="cacea-109">Az első parancs lekérte az eltávolítani kívánt kimenő szabálykonfigurációhoz társított terhelésegyenleg-elegyet, majd tárolja azt a $slb változóban.</span><span class="sxs-lookup"><span data-stu-id="cacea-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="cacea-110">A második parancs eltávolítja a kapcsolódó kimenő szabálykonfigurációt a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="cacea-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="cacea-111">A harmadik parancs frissíti a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="cacea-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="cacea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cacea-112">PARAMETERS</span></span>

### <span data-ttu-id="cacea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacea-113">-DefaultProfile</span></span>
<span data-ttu-id="cacea-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cacea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cacea-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cacea-115">-LoadBalancer</span></span>
<span data-ttu-id="cacea-116">A terheléselosztási erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="cacea-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="cacea-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cacea-117">-Name</span></span>
<span data-ttu-id="cacea-118">A kimenő szabály neve</span><span class="sxs-lookup"><span data-stu-id="cacea-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacea-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cacea-119">-Confirm</span></span>
<span data-ttu-id="cacea-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cacea-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cacea-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cacea-121">-WhatIf</span></span>
<span data-ttu-id="cacea-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cacea-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cacea-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cacea-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cacea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacea-124">CommonParameters</span></span>
<span data-ttu-id="cacea-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacea-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cacea-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacea-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cacea-127">INPUTS</span></span>

### <span data-ttu-id="cacea-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cacea-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cacea-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cacea-129">OUTPUTS</span></span>

### <span data-ttu-id="cacea-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cacea-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cacea-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cacea-131">NOTES</span></span>

## <span data-ttu-id="cacea-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cacea-132">RELATED LINKS</span></span>

[<span data-ttu-id="cacea-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cacea-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="cacea-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cacea-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="cacea-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cacea-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="cacea-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cacea-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
