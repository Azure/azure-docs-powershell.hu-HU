---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479915"
---
# <span data-ttu-id="7eca1-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eca1-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7eca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eca1-102">SYNOPSIS</span></span>
<span data-ttu-id="7eca1-103">Frissíti a terheléselosztás szabálykonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7eca1-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7eca1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7eca1-104">SYNTAX</span></span>

### <span data-ttu-id="7eca1-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7eca1-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eca1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7eca1-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eca1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7eca1-107">DESCRIPTION</span></span>
<span data-ttu-id="7eca1-108">A **Set-AzLoadBalancerRuleConfig** parancsmag frissíti a terheléselegyenlők szabálykonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7eca1-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7eca1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7eca1-109">EXAMPLES</span></span>

### <span data-ttu-id="7eca1-110">1. példa: Terheléselosztási szabály konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="7eca1-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="7eca1-111">Az első parancs lekérte a MyLoadBalancer nevű terheléselosztási törlőt, majd a $slb tárolja.</span><span class="sxs-lookup"><span data-stu-id="7eca1-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="7eca1-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az Add-AzLoadBalancerRuleConfig bővítménynek, amely hozzáad egy NewRule nevű szabályt.</span><span class="sxs-lookup"><span data-stu-id="7eca1-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="7eca1-113">A harmadik parancs átadja a terheléselegyenlőt a **Set-AzLoadBalancerRuleConfig** parancsnak, amely beállítja az új szabálykonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7eca1-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="7eca1-114">Vegye figyelembe, hogy a konfiguráció nem engedélyezi a lebegő IP-címeket, amelyeket az előző parancs engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="7eca1-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="7eca1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eca1-115">PARAMETERS</span></span>

### <span data-ttu-id="7eca1-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7eca1-116">-BackendAddressPool</span></span>
<span data-ttu-id="7eca1-117">Egy **BackendAddressPool** objektumot ad meg, amely terheléselosztási s szabályhoz társítható.</span><span class="sxs-lookup"><span data-stu-id="7eca1-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="7eca1-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7eca1-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="7eca1-119">Annak a **BackendAddressPool-objektumnak** az azonosítóját adja meg, amely a terheléselosztási szabály konfigurációjával társítható.</span><span class="sxs-lookup"><span data-stu-id="7eca1-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7eca1-120">-BackendPort</span></span>
<span data-ttu-id="7eca1-121">Az ezzel a szabálykonfigurációval egyező forgalom háttér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7eca1-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eca1-122">-DefaultProfile</span></span>
<span data-ttu-id="7eca1-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7eca1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eca1-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="7eca1-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="7eca1-125">Konfigurálja a SNAT-t a háttérkészletben található virtuális gépekhez úgy, hogy a terheléselosztási szabály előréjében megadott nyilvános IP-címet használják.</span><span class="sxs-lookup"><span data-stu-id="7eca1-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="7eca1-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7eca1-126">-EnableFloatingIP</span></span>
<span data-ttu-id="7eca1-127">Azt jelzi, hogy ez a parancsmag lebegő IP-címet tesz lehetővé egy szabálykonfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="7eca1-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7eca1-128">-EnableTcpReset</span></span>
<span data-ttu-id="7eca1-129">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="7eca1-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7eca1-130">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="7eca1-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7eca1-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7eca1-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7eca1-132">Megadja az előlapi IP-címek listáját, amelyek a terheléselosztási szabály konfigurációját társítják.</span><span class="sxs-lookup"><span data-stu-id="7eca1-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7eca1-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7eca1-134">Az előlapi IP-címek konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7eca1-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7eca1-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7eca1-135">-FrontendPort</span></span>
<span data-ttu-id="7eca1-136">Azt az előlapi portot adja meg, amelyet egy terheléselosztási szabály konfigurációja megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="7eca1-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7eca1-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7eca1-138">Azt adja meg percben, hogy a rendszer mely időtartamra tartja fenn a beszélgetések állapotát a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="7eca1-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="7eca1-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7eca1-139">-LoadBalancer</span></span>
<span data-ttu-id="7eca1-140">Terheléselosztást ad meg.</span><span class="sxs-lookup"><span data-stu-id="7eca1-140">Specifies a load balancer.</span></span>
<span data-ttu-id="7eca1-141">Ez a parancsmag frissíti a paraméter által megadott terheléselosztási szabálykonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7eca1-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7eca1-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="7eca1-142">-LoadDistribution</span></span>
<span data-ttu-id="7eca1-143">Terheléseloszlást ad meg.</span><span class="sxs-lookup"><span data-stu-id="7eca1-143">Specifies a load distribution.</span></span>
<span data-ttu-id="7eca1-144">A paraméter elfogadható értékei a következőek: SourceIP és SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="7eca1-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="7eca1-145">-Name</span><span class="sxs-lookup"><span data-stu-id="7eca1-145">-Name</span></span>
<span data-ttu-id="7eca1-146">A terheléselosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7eca1-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="7eca1-147">– Sivad</span><span class="sxs-lookup"><span data-stu-id="7eca1-147">-Probe</span></span>
<span data-ttu-id="7eca1-148">Egy terheléselosztási szabály konfigurációját társító adatbázist ad meg.</span><span class="sxs-lookup"><span data-stu-id="7eca1-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-149">-AzId-et</span><span class="sxs-lookup"><span data-stu-id="7eca1-149">-ProbeId</span></span>
<span data-ttu-id="7eca1-150">Megadja annak a konfigurációnak az azonosítóját, amely a terheléselosztási szabály konfigurációjával társítva van.</span><span class="sxs-lookup"><span data-stu-id="7eca1-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7eca1-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7eca1-151">-Protocol</span></span>
<span data-ttu-id="7eca1-152">Azt a protokollt adja meg, amelyet egy terheléselosztási szabály megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="7eca1-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="7eca1-153">A paraméter elfogadható értékei: Tcp vagy Udp.</span><span class="sxs-lookup"><span data-stu-id="7eca1-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7eca1-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7eca1-154">-Confirm</span></span>
<span data-ttu-id="7eca1-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7eca1-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eca1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eca1-156">-WhatIf</span></span>
<span data-ttu-id="7eca1-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7eca1-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7eca1-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7eca1-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eca1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eca1-159">CommonParameters</span></span>
<span data-ttu-id="7eca1-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eca1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eca1-161">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eca1-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eca1-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7eca1-162">INPUTS</span></span>

### <span data-ttu-id="7eca1-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7eca1-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7eca1-164">System.String</span><span class="sxs-lookup"><span data-stu-id="7eca1-164">System.String</span></span>

### <span data-ttu-id="7eca1-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7eca1-165">System.Int32</span></span>

### <span data-ttu-id="7eca1-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7eca1-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="7eca1-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7eca1-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="7eca1-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="7eca1-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="7eca1-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eca1-169">OUTPUTS</span></span>

### <span data-ttu-id="7eca1-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7eca1-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7eca1-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7eca1-171">NOTES</span></span>

## <span data-ttu-id="7eca1-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7eca1-172">RELATED LINKS</span></span>

[<span data-ttu-id="7eca1-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eca1-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7eca1-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eca1-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7eca1-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eca1-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7eca1-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eca1-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7eca1-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eca1-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


