---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b32f36e55df3c00ee7539c082f863be563b874b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941601"
---
# <span data-ttu-id="e6dbd-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6dbd-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e6dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e6dbd-103">A bejövő NAT-szabály konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="e6dbd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6dbd-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6dbd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="e6dbd-106">A **Remove-AzLoadBalancerInboundNatRuleConfig** parancsmag eltávolítja a bejövő hálózati címfordítási (NAT) szabálykonfigurációt az Azure terheléselegyenlőből.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="e6dbd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6dbd-107">EXAMPLES</span></span>

### <span data-ttu-id="e6dbd-108">1: Bejövő NAT-szabály törlése az Azure terheléselosztási szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="e6dbd-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e6dbd-109">Az első parancs betölt egy "mylb" nevű, már meglévő terhelésegyenleg-elosztást, és tárolja azt a $load változóban.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="e6dbd-110">A második parancs eltávolítja a terheléselosztáshoz társított bejövő NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="e6dbd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6dbd-111">PARAMETERS</span></span>

### <span data-ttu-id="e6dbd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6dbd-112">-DefaultProfile</span></span>
<span data-ttu-id="e6dbd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6dbd-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6dbd-114">-LoadBalancer</span></span>
<span data-ttu-id="e6dbd-115">Azt a **LoadBalancer-objektumot** adja meg, amely a parancsmag által eltávolított bejövő NAT-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6dbd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e6dbd-116">-Name</span></span>
<span data-ttu-id="e6dbd-117">Annak a bejövő NAT-szabály-konfigurációnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6dbd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6dbd-118">-Confirm</span></span>
<span data-ttu-id="e6dbd-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6dbd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6dbd-120">-WhatIf</span></span>
<span data-ttu-id="e6dbd-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6dbd-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6dbd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6dbd-123">CommonParameters</span></span>
<span data-ttu-id="e6dbd-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6dbd-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6dbd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6dbd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6dbd-126">INPUTS</span></span>

### <span data-ttu-id="e6dbd-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6dbd-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e6dbd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6dbd-128">OUTPUTS</span></span>

### <span data-ttu-id="e6dbd-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6dbd-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e6dbd-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6dbd-130">NOTES</span></span>

## <span data-ttu-id="e6dbd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6dbd-131">RELATED LINKS</span></span>

[<span data-ttu-id="e6dbd-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6dbd-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e6dbd-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6dbd-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e6dbd-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6dbd-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e6dbd-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6dbd-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


