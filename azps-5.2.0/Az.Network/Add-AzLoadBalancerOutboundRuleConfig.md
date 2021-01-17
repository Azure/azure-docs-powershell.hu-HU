---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365579"
---
# <span data-ttu-id="1854c-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1854c-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="1854c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1854c-102">SYNOPSIS</span></span>
<span data-ttu-id="1854c-103">Kimenő szabálykonfigurációt ad a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="1854c-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="1854c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1854c-104">SYNTAX</span></span>

### <span data-ttu-id="1854c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1854c-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1854c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1854c-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1854c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1854c-107">DESCRIPTION</span></span>
<span data-ttu-id="1854c-108">Az **Add-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt ad egy Azure-terheléselegyenlőhez.</span><span class="sxs-lookup"><span data-stu-id="1854c-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="1854c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1854c-109">EXAMPLES</span></span>

### <span data-ttu-id="1854c-110">1. példa: Kimenő szabálykonfiguráció hozzáadása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="1854c-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="1854c-111">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="1854c-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="1854c-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az **Add-AzLoadBalancerOutRuleConfig** bővítménynek, amely kimenő szabálykonfigurációt ad a terheléselegyenlőnek.</span><span class="sxs-lookup"><span data-stu-id="1854c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="1854c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1854c-113">PARAMETERS</span></span>

### <span data-ttu-id="1854c-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="1854c-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="1854c-115">A NAT-hoz használt kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="1854c-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="1854c-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1854c-116">-BackendAddressPool</span></span>
<span data-ttu-id="1854c-117">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="1854c-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="1854c-118">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="1854c-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="1854c-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1854c-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="1854c-120">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="1854c-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="1854c-121">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="1854c-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="1854c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1854c-122">-DefaultProfile</span></span>
<span data-ttu-id="1854c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1854c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1854c-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1854c-124">-EnableTcpReset</span></span>
<span data-ttu-id="1854c-125">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="1854c-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="1854c-126">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="1854c-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1854c-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1854c-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1854c-128">A terheléselosztás előlapi IP-címei.</span><span class="sxs-lookup"><span data-stu-id="1854c-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="1854c-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1854c-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1854c-130">A TCP-inaktív kapcsolat időkorlátja</span><span class="sxs-lookup"><span data-stu-id="1854c-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="1854c-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1854c-131">-LoadBalancer</span></span>
<span data-ttu-id="1854c-132">A terheléselosztási erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="1854c-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="1854c-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1854c-133">-Name</span></span>
<span data-ttu-id="1854c-134">A kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1854c-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="1854c-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1854c-135">-Protocol</span></span>
<span data-ttu-id="1854c-136">Protocol - TCP, UDP vagy All</span><span class="sxs-lookup"><span data-stu-id="1854c-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="1854c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1854c-137">-Confirm</span></span>
<span data-ttu-id="1854c-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1854c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1854c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1854c-139">-WhatIf</span></span>
<span data-ttu-id="1854c-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1854c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1854c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1854c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1854c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1854c-142">CommonParameters</span></span>
<span data-ttu-id="1854c-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1854c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1854c-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1854c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1854c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1854c-145">INPUTS</span></span>

### <span data-ttu-id="1854c-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1854c-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="1854c-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1854c-147">System.Int32</span></span>

### <span data-ttu-id="1854c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1854c-148">System.String</span></span>

### <span data-ttu-id="1854c-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="1854c-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="1854c-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1854c-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="1854c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1854c-151">OUTPUTS</span></span>

### <span data-ttu-id="1854c-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1854c-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1854c-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1854c-153">NOTES</span></span>

## <span data-ttu-id="1854c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1854c-154">RELATED LINKS</span></span>

[<span data-ttu-id="1854c-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1854c-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1854c-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1854c-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1854c-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1854c-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1854c-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1854c-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
