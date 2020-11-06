---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d76803df11ff3f89e20ca7d849577ca51331416c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498299"
---
# <span data-ttu-id="7a9b8-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a9b8-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="7a9b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9b8-103">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a9b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a9b8-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a9b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a9b8-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9b8-106">A **Remove-AzureRmLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt távolít el az Azure terheléselosztó szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="7a9b8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a9b8-107">EXAMPLES</span></span>

### <span data-ttu-id="7a9b8-108">1: a bejövő NAT-szabályok törlése Azure-terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="7a9b8-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7a9b8-109">Az első parancs betölti a már meglévő terheléselosztó nevű "mylb" nevű kiegyenlítőt, és a változót a $load kiegyensúlyozó változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="7a9b8-110">A második parancs eltávolítja a betöltőhöz társított bejövő NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="7a9b8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a9b8-111">PARAMETERS</span></span>

### <span data-ttu-id="7a9b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9b8-112">-DefaultProfile</span></span>
<span data-ttu-id="7a9b8-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a9b8-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a9b8-114">-LoadBalancer</span></span>
<span data-ttu-id="7a9b8-115">Azt a **LoadBalancer** -objektumot adja meg, amely a parancsmag által eltávolított bejövő címfordítási szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a9b8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a9b8-116">-Name</span></span>
<span data-ttu-id="7a9b8-117">Annak a bejövő CÍMFORDÍTÁSi szabály konfigurációjának a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a9b8-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a9b8-118">-Confirm</span></span>
<span data-ttu-id="7a9b8-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a9b8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a9b8-120">-WhatIf</span></span>
<span data-ttu-id="7a9b8-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a9b8-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a9b8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a9b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9b8-123">CommonParameters</span></span>
<span data-ttu-id="7a9b8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a9b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9b8-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9b8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a9b8-126">INPUTS</span></span>

### <span data-ttu-id="7a9b8-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a9b8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="7a9b8-128">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a9b8-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="7a9b8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a9b8-129">OUTPUTS</span></span>

### <span data-ttu-id="7a9b8-130">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7a9b8-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7a9b8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a9b8-131">NOTES</span></span>

## <span data-ttu-id="7a9b8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a9b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="7a9b8-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a9b8-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7a9b8-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a9b8-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7a9b8-135">Új – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a9b8-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7a9b8-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7a9b8-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


