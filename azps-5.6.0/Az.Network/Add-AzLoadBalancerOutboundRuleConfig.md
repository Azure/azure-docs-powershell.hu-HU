---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006486"
---
# <span data-ttu-id="69151-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69151-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="69151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69151-102">SYNOPSIS</span></span>
<span data-ttu-id="69151-103">Kimenő szabálykonfigurációt ad a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="69151-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="69151-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69151-104">SYNTAX</span></span>

### <span data-ttu-id="69151-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69151-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69151-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69151-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69151-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69151-107">DESCRIPTION</span></span>
<span data-ttu-id="69151-108">Az **Add-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt ad egy Azure-terheléselegyenlőhez.</span><span class="sxs-lookup"><span data-stu-id="69151-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="69151-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69151-109">EXAMPLES</span></span>

### <span data-ttu-id="69151-110">1. példa: Kimenő szabálykonfiguráció hozzáadása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="69151-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="69151-111">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="69151-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="69151-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az **Add-AzLoadBalancerOutRuleConfig** bővítménynek, amely kimenő szabálykonfigurációt ad a terheléselegyenlőnek.</span><span class="sxs-lookup"><span data-stu-id="69151-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="69151-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69151-113">PARAMETERS</span></span>

### <span data-ttu-id="69151-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="69151-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="69151-115">A NAT-hoz használt kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="69151-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="69151-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="69151-116">-BackendAddressPool</span></span>
<span data-ttu-id="69151-117">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="69151-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="69151-118">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="69151-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="69151-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="69151-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="69151-120">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="69151-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="69151-121">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="69151-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="69151-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69151-122">-DefaultProfile</span></span>
<span data-ttu-id="69151-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69151-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69151-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="69151-124">-EnableTcpReset</span></span>
<span data-ttu-id="69151-125">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="69151-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="69151-126">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="69151-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="69151-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="69151-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="69151-128">A terheléselosztás előlapi IP-címei.</span><span class="sxs-lookup"><span data-stu-id="69151-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="69151-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="69151-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="69151-130">A TCP-inaktív kapcsolat időkorlátja</span><span class="sxs-lookup"><span data-stu-id="69151-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="69151-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69151-131">-LoadBalancer</span></span>
<span data-ttu-id="69151-132">A terheléselosztási erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="69151-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="69151-133">-Name</span><span class="sxs-lookup"><span data-stu-id="69151-133">-Name</span></span>
<span data-ttu-id="69151-134">A kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="69151-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="69151-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="69151-135">-Protocol</span></span>
<span data-ttu-id="69151-136">Protocol - TCP, UDP vagy All</span><span class="sxs-lookup"><span data-stu-id="69151-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="69151-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69151-137">-Confirm</span></span>
<span data-ttu-id="69151-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69151-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69151-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69151-139">-WhatIf</span></span>
<span data-ttu-id="69151-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69151-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69151-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69151-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69151-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69151-142">CommonParameters</span></span>
<span data-ttu-id="69151-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69151-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69151-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69151-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69151-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69151-145">INPUTS</span></span>

### <span data-ttu-id="69151-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69151-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="69151-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="69151-147">System.Int32</span></span>

### <span data-ttu-id="69151-148">System.String</span><span class="sxs-lookup"><span data-stu-id="69151-148">System.String</span></span>

### <span data-ttu-id="69151-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="69151-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="69151-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="69151-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="69151-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69151-151">OUTPUTS</span></span>

### <span data-ttu-id="69151-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69151-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="69151-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69151-153">NOTES</span></span>

## <span data-ttu-id="69151-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69151-154">RELATED LINKS</span></span>

[<span data-ttu-id="69151-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69151-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="69151-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69151-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="69151-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69151-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="69151-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69151-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
