---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 053f86f0b29346c98f60a3160a8e1f2a51ab0e14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941594"
---
# <span data-ttu-id="ea3a8-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea3a8-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="ea3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3a8-103">Eltávolít egy szabálykonfigurációt a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ea3a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea3a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea3a8-106">A **Remove-AzLoadBalancerRuleConfig** parancsmag eltávolítja egy Azure-terheléselegyenlő szabálykonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ea3a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea3a8-107">EXAMPLES</span></span>

### <span data-ttu-id="ea3a8-108">1. példa: Szabálykonfiguráció eltávolítása terheléselosztásról</span><span class="sxs-lookup"><span data-stu-id="ea3a8-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ea3a8-109">Az első parancs lekérte a MyLoadBalancer nevű terheléselosztási törlőt, majd a $loadbalancer tárolja.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="ea3a8-110">A második parancs eltávolítja a MyLName nevű szabálykonfigurációt a rendszer terheléselosztási $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ea3a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-111">PARAMETERS</span></span>

### <span data-ttu-id="ea3a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3a8-112">-DefaultProfile</span></span>
<span data-ttu-id="ea3a8-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea3a8-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea3a8-114">-LoadBalancer</span></span>
<span data-ttu-id="ea3a8-115">Azt a **LoadBalancer-objektumot** adja meg, amely a parancsmag által eltávolított szabálykonfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea3a8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ea3a8-116">-Name</span></span>
<span data-ttu-id="ea3a8-117">A parancsmag által eltávolított terheléselosztási szabálykonfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea3a8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea3a8-118">-Confirm</span></span>
<span data-ttu-id="ea3a8-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea3a8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea3a8-120">-WhatIf</span></span>
<span data-ttu-id="ea3a8-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea3a8-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea3a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3a8-123">CommonParameters</span></span>
<span data-ttu-id="ea3a8-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3a8-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea3a8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3a8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-126">INPUTS</span></span>

### <span data-ttu-id="ea3a8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea3a8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ea3a8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea3a8-128">OUTPUTS</span></span>

### <span data-ttu-id="ea3a8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea3a8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ea3a8-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea3a8-130">NOTES</span></span>

## <span data-ttu-id="ea3a8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea3a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea3a8-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea3a8-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ea3a8-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea3a8-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ea3a8-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea3a8-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ea3a8-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea3a8-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ea3a8-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea3a8-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


