---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194911"
---
# <span data-ttu-id="c50f1-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c50f1-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c50f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c50f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c50f1-103">A terheléselosztó szabályait frissíti.</span><span class="sxs-lookup"><span data-stu-id="c50f1-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c50f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c50f1-104">SYNTAX</span></span>

### <span data-ttu-id="c50f1-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c50f1-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c50f1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c50f1-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c50f1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c50f1-107">DESCRIPTION</span></span>
<span data-ttu-id="c50f1-108">A **set-AzLoadBalancerRuleConfig** parancsmag frissíti a terheléselosztási szabályok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c50f1-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c50f1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c50f1-109">EXAMPLES</span></span>

### <span data-ttu-id="c50f1-110">Példa 1: terheléselosztási szabály konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="c50f1-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="c50f1-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c50f1-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c50f1-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerRuleConfig-hoz, amely egy NewRule nevű szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c50f1-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="c50f1-113">A harmadik parancs átadja a terheléselosztó **beállítást a set-AzLoadBalancerRuleConfig** , amely az új szabály konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="c50f1-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="c50f1-114">Ne feledje, hogy a konfiguráció nem engedélyezi az előző parancs által engedélyezett lebegő IP-címet.</span><span class="sxs-lookup"><span data-stu-id="c50f1-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="c50f1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c50f1-115">PARAMETERS</span></span>

### <span data-ttu-id="c50f1-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c50f1-116">-BackendAddressPool</span></span>
<span data-ttu-id="c50f1-117">A terheléselosztási szabályokhoz társítani kívánt **BackendAddressPool** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c50f1-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c50f1-119">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="c50f1-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c50f1-120">-BackendPort</span></span>
<span data-ttu-id="c50f1-121">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="c50f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50f1-122">-DefaultProfile</span></span>
<span data-ttu-id="c50f1-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c50f1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c50f1-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c50f1-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c50f1-125">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="c50f1-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c50f1-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c50f1-126">-EnableFloatingIP</span></span>
<span data-ttu-id="c50f1-127">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="c50f1-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c50f1-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c50f1-128">-EnableTcpReset</span></span>
<span data-ttu-id="c50f1-129">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="c50f1-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c50f1-130">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="c50f1-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c50f1-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c50f1-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c50f1-132">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c50f1-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c50f1-134">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-134">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c50f1-135">-FrontendPort</span></span>
<span data-ttu-id="c50f1-136">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c50f1-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c50f1-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c50f1-138">Azt adja meg, hogy hány percen belül maradjon a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="c50f1-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c50f1-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50f1-139">-LoadBalancer</span></span>
<span data-ttu-id="c50f1-140">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-140">Specifies a load balancer.</span></span>
<span data-ttu-id="c50f1-141">Ez a parancsmag frissíti a paraméter által megadott terheléselosztó szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c50f1-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c50f1-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c50f1-142">-LoadDistribution</span></span>
<span data-ttu-id="c50f1-143">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-143">Specifies a load distribution.</span></span>
<span data-ttu-id="c50f1-144">A paraméter elfogadható értékei a következők: SourceIP és SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="c50f1-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c50f1-145">-Name</span></span>
<span data-ttu-id="c50f1-146">A terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="c50f1-147">-Szonda</span><span class="sxs-lookup"><span data-stu-id="c50f1-147">-Probe</span></span>
<span data-ttu-id="c50f1-148">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c50f1-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c50f1-149">-ProbeId</span></span>
<span data-ttu-id="c50f1-150">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="c50f1-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c50f1-151">-Protocol</span></span>
<span data-ttu-id="c50f1-152">A terheléselosztási szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50f1-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="c50f1-153">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="c50f1-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50f1-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c50f1-154">-Confirm</span></span>
<span data-ttu-id="c50f1-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c50f1-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c50f1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c50f1-156">-WhatIf</span></span>
<span data-ttu-id="c50f1-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c50f1-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c50f1-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c50f1-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c50f1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50f1-159">CommonParameters</span></span>
<span data-ttu-id="c50f1-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c50f1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50f1-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c50f1-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50f1-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c50f1-162">INPUTS</span></span>

### <span data-ttu-id="c50f1-163">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50f1-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c50f1-164">System. String</span><span class="sxs-lookup"><span data-stu-id="c50f1-164">System.String</span></span>

### <span data-ttu-id="c50f1-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c50f1-165">System.Int32</span></span>

### <span data-ttu-id="c50f1-166">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c50f1-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="c50f1-167">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c50f1-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="c50f1-168">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="c50f1-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="c50f1-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c50f1-169">OUTPUTS</span></span>

### <span data-ttu-id="c50f1-170">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50f1-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c50f1-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c50f1-171">NOTES</span></span>

## <span data-ttu-id="c50f1-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c50f1-172">RELATED LINKS</span></span>

[<span data-ttu-id="c50f1-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c50f1-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c50f1-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c50f1-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c50f1-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c50f1-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c50f1-176">Új – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c50f1-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c50f1-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c50f1-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

