---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 2d47a3481772d846a65e3b0bc0d1eb1c62fa5cd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670159"
---
# <span data-ttu-id="3dde1-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dde1-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="3dde1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3dde1-102">SYNOPSIS</span></span>
<span data-ttu-id="3dde1-103">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="3dde1-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="3dde1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3dde1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dde1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3dde1-105">DESCRIPTION</span></span>
<span data-ttu-id="3dde1-106">A **Remove-AzLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt távolít el az Azure terheléselosztó szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="3dde1-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="3dde1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3dde1-107">EXAMPLES</span></span>

### <span data-ttu-id="3dde1-108">1: a bejövő NAT-szabályok törlése Azure-terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="3dde1-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="3dde1-109">Az első parancs betölti a már meglévő terheléselosztó nevű "mylb" nevű kiegyenlítőt, és a változót a $load kiegyensúlyozó változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3dde1-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="3dde1-110">A második parancs eltávolítja a betöltőhöz társított bejövő NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="3dde1-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="3dde1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3dde1-111">PARAMETERS</span></span>

### <span data-ttu-id="3dde1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dde1-112">-DefaultProfile</span></span>
<span data-ttu-id="3dde1-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3dde1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dde1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dde1-114">-LoadBalancer</span></span>
<span data-ttu-id="3dde1-115">Azt a **LoadBalancer** -objektumot adja meg, amely a parancsmag által eltávolított bejövő címfordítási szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3dde1-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3dde1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3dde1-116">-Name</span></span>
<span data-ttu-id="3dde1-117">Annak a bejövő CÍMFORDÍTÁSi szabály konfigurációjának a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3dde1-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3dde1-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3dde1-118">-Confirm</span></span>
<span data-ttu-id="3dde1-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3dde1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dde1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dde1-120">-WhatIf</span></span>
<span data-ttu-id="3dde1-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3dde1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dde1-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3dde1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dde1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dde1-123">CommonParameters</span></span>
<span data-ttu-id="3dde1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3dde1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dde1-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dde1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dde1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dde1-126">INPUTS</span></span>

### <span data-ttu-id="3dde1-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dde1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3dde1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dde1-128">OUTPUTS</span></span>

### <span data-ttu-id="3dde1-129">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dde1-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3dde1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3dde1-130">NOTES</span></span>

## <span data-ttu-id="3dde1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dde1-131">RELATED LINKS</span></span>

[<span data-ttu-id="3dde1-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dde1-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3dde1-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dde1-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3dde1-134">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dde1-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3dde1-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dde1-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


