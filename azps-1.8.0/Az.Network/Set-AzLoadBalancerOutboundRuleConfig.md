---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 482f729f0ee3fa3efc6a78a1bc2b5fbbd3fe1d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670003"
---
# <span data-ttu-id="65205-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65205-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="65205-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65205-102">SYNOPSIS</span></span>
<span data-ttu-id="65205-103">Kimenő szabály konfigurációját állítja be a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="65205-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="65205-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65205-104">SYNTAX</span></span>

### <span data-ttu-id="65205-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65205-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65205-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65205-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65205-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="65205-107">DESCRIPTION</span></span>
<span data-ttu-id="65205-108">A **set-AzLoadBalancerOutboundRuleConfig** parancsmag az Azure terheléselosztás kimenő szabályainak konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="65205-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="65205-109">Példák</span><span class="sxs-lookup"><span data-stu-id="65205-109">EXAMPLES</span></span>

### <span data-ttu-id="65205-110">Példa 1: a Kimenő szabály konfigurációjának módosítása a terheléselosztó eszközön</span><span class="sxs-lookup"><span data-stu-id="65205-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="65205-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="65205-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="65205-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb-AzLoadBalancerOutboundRuleConfig, amely kimenő szabály konfigurációját adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="65205-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="65205-113">A harmadik parancs átadja a terheléselosztó **beállítást a set-AzLoadBalancerOutboundRuleConfig** , amely a Kimenő szabály konfigurációját menti és frissíti.</span><span class="sxs-lookup"><span data-stu-id="65205-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="65205-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65205-114">PARAMETERS</span></span>

### <span data-ttu-id="65205-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="65205-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="65205-116">A NAT-hoz használandó kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="65205-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="65205-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="65205-117">-BackendAddressPool</span></span>
<span data-ttu-id="65205-118">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="65205-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="65205-119">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="65205-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="65205-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="65205-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="65205-121">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="65205-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="65205-122">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="65205-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="65205-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65205-123">-DefaultProfile</span></span>
<span data-ttu-id="65205-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65205-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65205-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="65205-125">-EnableTcpReset</span></span>
<span data-ttu-id="65205-126">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="65205-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="65205-127">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="65205-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="65205-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="65205-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="65205-129">A terheléselosztó IP-címei.</span><span class="sxs-lookup"><span data-stu-id="65205-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="65205-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="65205-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="65205-131">A TCP üresjárati kapcsolat időtúllépése</span><span class="sxs-lookup"><span data-stu-id="65205-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="65205-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65205-132">-LoadBalancer</span></span>
<span data-ttu-id="65205-133">A terheléselosztó erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="65205-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="65205-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65205-134">-Name</span></span>
<span data-ttu-id="65205-135">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="65205-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="65205-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="65205-136">-Protocol</span></span>
<span data-ttu-id="65205-137">Protocol – TCP, UDP vagy mind</span><span class="sxs-lookup"><span data-stu-id="65205-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="65205-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65205-138">-Confirm</span></span>
<span data-ttu-id="65205-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65205-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65205-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65205-140">-WhatIf</span></span>
<span data-ttu-id="65205-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65205-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65205-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65205-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65205-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65205-143">CommonParameters</span></span>
<span data-ttu-id="65205-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65205-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65205-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65205-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65205-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65205-146">INPUTS</span></span>

### <span data-ttu-id="65205-147">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65205-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="65205-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="65205-148">System.Int32</span></span>

### <span data-ttu-id="65205-149">System. String</span><span class="sxs-lookup"><span data-stu-id="65205-149">System.String</span></span>

### <span data-ttu-id="65205-150">Microsoft. Azure. commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="65205-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="65205-151">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="65205-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="65205-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65205-152">OUTPUTS</span></span>

### <span data-ttu-id="65205-153">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65205-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="65205-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65205-154">NOTES</span></span>

## <span data-ttu-id="65205-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65205-155">RELATED LINKS</span></span>

[<span data-ttu-id="65205-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65205-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="65205-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65205-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="65205-158">Új – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65205-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="65205-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65205-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
