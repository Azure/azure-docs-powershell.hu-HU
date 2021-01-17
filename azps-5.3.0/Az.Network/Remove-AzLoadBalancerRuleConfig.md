---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468890"
---
# <span data-ttu-id="75cac-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75cac-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="75cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cac-102">SYNOPSIS</span></span>
<span data-ttu-id="75cac-103">Eltávolít egy szabálykonfigurációt a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="75cac-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="75cac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75cac-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75cac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75cac-105">DESCRIPTION</span></span>
<span data-ttu-id="75cac-106">A **Remove-AzLoadBalancerRuleConfig** parancsmag eltávolítja egy Azure-terheléselegyenlő szabálykonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="75cac-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="75cac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75cac-107">EXAMPLES</span></span>

### <span data-ttu-id="75cac-108">1. példa: Szabálykonfiguráció eltávolítása terheléselosztásról</span><span class="sxs-lookup"><span data-stu-id="75cac-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="75cac-109">Az első parancs lekérte a MyLoadBalancer nevű terheléselosztási törlőt, majd a $loadbalancer tárolja.</span><span class="sxs-lookup"><span data-stu-id="75cac-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="75cac-110">A második parancs eltávolítja a MyLName nevű szabálykonfigurációt a rendszer terheléselosztási $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="75cac-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="75cac-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cac-111">PARAMETERS</span></span>

### <span data-ttu-id="75cac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cac-112">-DefaultProfile</span></span>
<span data-ttu-id="75cac-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75cac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75cac-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75cac-114">-LoadBalancer</span></span>
<span data-ttu-id="75cac-115">Azt a **LoadBalancer-objektumot** adja meg, amely a parancsmag által eltávolított szabálykonfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="75cac-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="75cac-116">-Name</span><span class="sxs-lookup"><span data-stu-id="75cac-116">-Name</span></span>
<span data-ttu-id="75cac-117">A parancsmag által eltávolított terheléselosztási szabálykonfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75cac-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="75cac-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75cac-118">-Confirm</span></span>
<span data-ttu-id="75cac-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75cac-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cac-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cac-120">-WhatIf</span></span>
<span data-ttu-id="75cac-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75cac-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75cac-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75cac-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cac-123">CommonParameters</span></span>
<span data-ttu-id="75cac-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cac-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75cac-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cac-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75cac-126">INPUTS</span></span>

### <span data-ttu-id="75cac-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75cac-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="75cac-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75cac-128">OUTPUTS</span></span>

### <span data-ttu-id="75cac-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75cac-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="75cac-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75cac-130">NOTES</span></span>

## <span data-ttu-id="75cac-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75cac-131">RELATED LINKS</span></span>

[<span data-ttu-id="75cac-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75cac-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="75cac-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75cac-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="75cac-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75cac-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="75cac-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75cac-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="75cac-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75cac-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


