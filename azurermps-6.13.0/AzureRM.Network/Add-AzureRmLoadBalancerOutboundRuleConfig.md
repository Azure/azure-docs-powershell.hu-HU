---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ac96a07fb7ec32589ac351fc592c4c2848e75978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493656"
---
# <span data-ttu-id="83b43-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="83b43-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="83b43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83b43-102">SYNOPSIS</span></span>
<span data-ttu-id="83b43-103">Kimenő szabály konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="83b43-103">Adds an outbound rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83b43-104">SYNTAX</span></span>

### <span data-ttu-id="83b43-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83b43-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83b43-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="83b43-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83b43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83b43-107">DESCRIPTION</span></span>
<span data-ttu-id="83b43-108">Az **Add-AzureRmLoadBalancerOutboundRuleConfig** parancsmag egy kimenő szabály-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="83b43-108">The **Add-AzureRmLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="83b43-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83b43-109">EXAMPLES</span></span>

### <span data-ttu-id="83b43-110">1. példa: Kimenő szabály konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="83b43-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="83b43-111">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="83b43-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="83b43-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a **AzureRmLoadBalancerOutboundRuleConfig-** hoz, amely egy kimenő szabály konfigurációját hozzáadja a terheléselosztó bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="83b43-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="83b43-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83b43-113">PARAMETERS</span></span>

### <span data-ttu-id="83b43-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="83b43-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="83b43-115">A NAT-hoz használandó kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="83b43-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="83b43-116">-BackendAddressPool</span></span>
<span data-ttu-id="83b43-117">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="83b43-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="83b43-118">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="83b43-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="83b43-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="83b43-120">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="83b43-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="83b43-121">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="83b43-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b43-122">-DefaultProfile</span></span>
<span data-ttu-id="83b43-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83b43-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b43-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="83b43-124">-EnableTcpReset</span></span>
<span data-ttu-id="83b43-125">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="83b43-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="83b43-126">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="83b43-126">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="83b43-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="83b43-128">A terheléselosztó IP-címei.</span><span class="sxs-lookup"><span data-stu-id="83b43-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="83b43-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="83b43-130">A TCP üresjárati kapcsolat időtúllépése</span><span class="sxs-lookup"><span data-stu-id="83b43-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83b43-131">-LoadBalancer</span></span>
<span data-ttu-id="83b43-132">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="83b43-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="83b43-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83b43-133">-Name</span></span>
<span data-ttu-id="83b43-134">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="83b43-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="83b43-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="83b43-135">-Protocol</span></span>
<span data-ttu-id="83b43-136">Protocol – TCP, UDP vagy mind</span><span class="sxs-lookup"><span data-stu-id="83b43-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b43-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83b43-137">-Confirm</span></span>
<span data-ttu-id="83b43-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83b43-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b43-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b43-139">-WhatIf</span></span>
<span data-ttu-id="83b43-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83b43-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b43-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83b43-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b43-142">CommonParameters</span></span>
<span data-ttu-id="83b43-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83b43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b43-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b43-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b43-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83b43-145">INPUTS</span></span>

### <span data-ttu-id="83b43-146">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83b43-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="83b43-147">System. Int32 System. String System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSResourceId, Microsoft. Azure. commands. Network, Version = 6.5.0.0, Culture = semleges, PublicKeyToken = null]] Microsoft. Azure. Command. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="83b43-147">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="83b43-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83b43-148">OUTPUTS</span></span>

### <span data-ttu-id="83b43-149">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83b43-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="83b43-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83b43-150">NOTES</span></span>

## <span data-ttu-id="83b43-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83b43-151">RELATED LINKS</span></span>
