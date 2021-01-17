---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479916"
---
# <span data-ttu-id="36656-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36656-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="36656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36656-102">SYNOPSIS</span></span>
<span data-ttu-id="36656-103">Kimenő szabálykonfigurációt állít be egy terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="36656-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="36656-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36656-104">SYNTAX</span></span>

### <span data-ttu-id="36656-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36656-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36656-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36656-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36656-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36656-107">DESCRIPTION</span></span>
<span data-ttu-id="36656-108">A **Set-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt állít be egy Azure terheléselegyenlő számára.</span><span class="sxs-lookup"><span data-stu-id="36656-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="36656-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36656-109">EXAMPLES</span></span>

### <span data-ttu-id="36656-110">1. példa: A kimenő szabály konfigurációjának módosítása terheléselosztáson</span><span class="sxs-lookup"><span data-stu-id="36656-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="36656-111">Az első parancs lekérte a MyLoadBalancer nevű terheléselosztási törlőt, majd a $slb tárolja.</span><span class="sxs-lookup"><span data-stu-id="36656-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="36656-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az Add-AzLoadBalancerOutRuleConfig bővítménynek, amely egy kimenő szabálykonfigurációt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="36656-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="36656-113">A harmadik parancs átadja a terheléselegyenlőt a **Set-AzLoadBalancerOutboundRuleConfig** parancsnak, amely menti és frissíti a kimenő szabálykonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="36656-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="36656-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36656-114">PARAMETERS</span></span>

### <span data-ttu-id="36656-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="36656-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="36656-116">A NAT-hoz használt kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="36656-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="36656-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="36656-117">-BackendAddressPool</span></span>
<span data-ttu-id="36656-118">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="36656-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="36656-119">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="36656-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="36656-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="36656-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="36656-121">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="36656-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="36656-122">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="36656-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="36656-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36656-123">-DefaultProfile</span></span>
<span data-ttu-id="36656-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36656-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36656-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="36656-125">-EnableTcpReset</span></span>
<span data-ttu-id="36656-126">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="36656-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="36656-127">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="36656-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="36656-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="36656-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="36656-129">A terheléselosztás előlapi IP-címei.</span><span class="sxs-lookup"><span data-stu-id="36656-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="36656-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="36656-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="36656-131">A TCP-inaktív kapcsolat időkorlátja</span><span class="sxs-lookup"><span data-stu-id="36656-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="36656-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36656-132">-LoadBalancer</span></span>
<span data-ttu-id="36656-133">A terheléselosztási erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="36656-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="36656-134">-Name</span><span class="sxs-lookup"><span data-stu-id="36656-134">-Name</span></span>
<span data-ttu-id="36656-135">A kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="36656-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="36656-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="36656-136">-Protocol</span></span>
<span data-ttu-id="36656-137">Protocol - TCP, UDP vagy All</span><span class="sxs-lookup"><span data-stu-id="36656-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="36656-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36656-138">-Confirm</span></span>
<span data-ttu-id="36656-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36656-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36656-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36656-140">-WhatIf</span></span>
<span data-ttu-id="36656-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36656-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36656-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36656-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36656-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36656-143">CommonParameters</span></span>
<span data-ttu-id="36656-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36656-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36656-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36656-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36656-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36656-146">INPUTS</span></span>

### <span data-ttu-id="36656-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36656-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="36656-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="36656-148">System.Int32</span></span>

### <span data-ttu-id="36656-149">System.String</span><span class="sxs-lookup"><span data-stu-id="36656-149">System.String</span></span>

### <span data-ttu-id="36656-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="36656-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="36656-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="36656-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="36656-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36656-152">OUTPUTS</span></span>

### <span data-ttu-id="36656-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36656-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="36656-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36656-154">NOTES</span></span>

## <span data-ttu-id="36656-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36656-155">RELATED LINKS</span></span>

[<span data-ttu-id="36656-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36656-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="36656-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36656-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="36656-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36656-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="36656-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36656-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
