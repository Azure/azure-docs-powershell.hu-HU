---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 01e132dab83931a48254bb8483cc794d7c619a6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837852"
---
# <span data-ttu-id="4924a-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4924a-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4924a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4924a-102">SYNOPSIS</span></span>
<span data-ttu-id="4924a-103">Új szabály konfigurációjának eltávolítása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="4924a-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4924a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4924a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4924a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4924a-105">DESCRIPTION</span></span>
<span data-ttu-id="4924a-106">A **Remove-AzLoadBalancerRuleConfig** parancsmag eltávolítja az Azure-terheléselosztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4924a-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4924a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4924a-107">EXAMPLES</span></span>

### <span data-ttu-id="4924a-108">1. példa: szabály-konfiguráció eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="4924a-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4924a-109">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4924a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="4924a-110">A második parancs eltávolítja a MyLBruleName nevű szabály-konfigurációt a $loadbalancer terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="4924a-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4924a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4924a-111">PARAMETERS</span></span>

### <span data-ttu-id="4924a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4924a-112">-DefaultProfile</span></span>
<span data-ttu-id="4924a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4924a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4924a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4924a-114">-LoadBalancer</span></span>
<span data-ttu-id="4924a-115">Azt a **LoadBalancer** objektumot adja meg, amely a parancsmag által eltávolított szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4924a-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4924a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4924a-116">-Name</span></span>
<span data-ttu-id="4924a-117">Annak a terheléselosztó szabály-konfigurációnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4924a-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4924a-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4924a-118">-Confirm</span></span>
<span data-ttu-id="4924a-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4924a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4924a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4924a-120">-WhatIf</span></span>
<span data-ttu-id="4924a-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4924a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4924a-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4924a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4924a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4924a-123">CommonParameters</span></span>
<span data-ttu-id="4924a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4924a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4924a-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4924a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4924a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4924a-126">INPUTS</span></span>

### <span data-ttu-id="4924a-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4924a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4924a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4924a-128">OUTPUTS</span></span>

### <span data-ttu-id="4924a-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4924a-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4924a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4924a-130">NOTES</span></span>

## <span data-ttu-id="4924a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4924a-131">RELATED LINKS</span></span>

[<span data-ttu-id="4924a-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4924a-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4924a-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4924a-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4924a-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4924a-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4924a-135">Új – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4924a-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4924a-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4924a-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


