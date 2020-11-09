---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303758"
---
# <span data-ttu-id="69967-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69967-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="69967-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69967-102">SYNOPSIS</span></span>
<span data-ttu-id="69967-103">Kimenő szabály konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="69967-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="69967-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69967-104">SYNTAX</span></span>

### <span data-ttu-id="69967-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69967-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69967-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69967-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69967-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="69967-107">DESCRIPTION</span></span>
<span data-ttu-id="69967-108">Az **Add-AzLoadBalancerOutboundRuleConfig** parancsmag egy kimenő szabály-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="69967-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="69967-109">Példák</span><span class="sxs-lookup"><span data-stu-id="69967-109">EXAMPLES</span></span>

### <span data-ttu-id="69967-110">1. példa: Kimenő szabály konfigurációjának hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="69967-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="69967-111">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="69967-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="69967-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a **AzLoadBalancerOutboundRuleConfig-** hoz, amely egy kimenő szabály konfigurációját hozzáadja a terheléselosztó bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="69967-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="69967-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69967-113">PARAMETERS</span></span>

### <span data-ttu-id="69967-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="69967-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="69967-115">A NAT-hoz használandó kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="69967-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="69967-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="69967-116">-BackendAddressPool</span></span>
<span data-ttu-id="69967-117">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="69967-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="69967-118">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="69967-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="69967-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="69967-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="69967-120">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="69967-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="69967-121">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="69967-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="69967-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69967-122">-DefaultProfile</span></span>
<span data-ttu-id="69967-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69967-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69967-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="69967-124">-EnableTcpReset</span></span>
<span data-ttu-id="69967-125">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="69967-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="69967-126">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="69967-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="69967-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="69967-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="69967-128">A terheléselosztó IP-címei.</span><span class="sxs-lookup"><span data-stu-id="69967-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69967-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="69967-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="69967-130">A TCP üresjárati kapcsolat időtúllépése</span><span class="sxs-lookup"><span data-stu-id="69967-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="69967-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69967-131">-LoadBalancer</span></span>
<span data-ttu-id="69967-132">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="69967-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="69967-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69967-133">-Name</span></span>
<span data-ttu-id="69967-134">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="69967-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="69967-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="69967-135">-Protocol</span></span>
<span data-ttu-id="69967-136">Protocol – TCP, UDP vagy mind</span><span class="sxs-lookup"><span data-stu-id="69967-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="69967-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69967-137">-Confirm</span></span>
<span data-ttu-id="69967-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69967-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69967-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69967-139">-WhatIf</span></span>
<span data-ttu-id="69967-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69967-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69967-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69967-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69967-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69967-142">CommonParameters</span></span>
<span data-ttu-id="69967-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69967-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69967-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69967-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69967-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69967-145">INPUTS</span></span>

### <span data-ttu-id="69967-146">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69967-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="69967-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="69967-147">System.Int32</span></span>

### <span data-ttu-id="69967-148">System. String</span><span class="sxs-lookup"><span data-stu-id="69967-148">System.String</span></span>

### <span data-ttu-id="69967-149">Microsoft. Azure. commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="69967-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="69967-150">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="69967-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="69967-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69967-151">OUTPUTS</span></span>

### <span data-ttu-id="69967-152">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69967-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="69967-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69967-153">NOTES</span></span>

## <span data-ttu-id="69967-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69967-154">RELATED LINKS</span></span>

[<span data-ttu-id="69967-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69967-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="69967-156">Új – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69967-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="69967-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69967-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="69967-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69967-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
