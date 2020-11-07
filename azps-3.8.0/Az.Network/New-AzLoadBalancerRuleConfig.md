---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d93bf82421851a79399061861ed9f2ca29d9a5c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845233"
---
# <span data-ttu-id="a75e9-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a75e9-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a75e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a75e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a75e9-103">Szabály-konfigurációt hoz létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="a75e9-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a75e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a75e9-104">SYNTAX</span></span>

### <span data-ttu-id="a75e9-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a75e9-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a75e9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a75e9-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a75e9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a75e9-107">DESCRIPTION</span></span>
<span data-ttu-id="a75e9-108">A **New-AzLoadBalancerRuleConfig** parancsmag létrehoz egy szabály-konfigurációt az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="a75e9-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a75e9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a75e9-109">EXAMPLES</span></span>

### <span data-ttu-id="a75e9-110">1: szabály-konfiguráció létrehozása Azure-terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="a75e9-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="a75e9-111">Az első három parancs a nyilvános IP-címet, az előtér-előnézetet, valamint a szabály konfigurációjának megfelelő szondát tartalmaz a Forth parancsban.</span><span class="sxs-lookup"><span data-stu-id="a75e9-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="a75e9-112">A Forth parancs új szabályt hoz létre, amelynek neve MyLBrule bizonyos előírásokkal.</span><span class="sxs-lookup"><span data-stu-id="a75e9-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="a75e9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a75e9-113">PARAMETERS</span></span>

### <span data-ttu-id="a75e9-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a75e9-114">-BackendAddressPool</span></span>
<span data-ttu-id="a75e9-115">Itt adhatja meg azt a **BackendAddressPool** -objektumot, amellyel társítani szeretné a terheléselosztó szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a75e9-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a75e9-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="a75e9-117">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="a75e9-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a75e9-118">-BackendPort</span></span>
<span data-ttu-id="a75e9-119">A terheléselosztási szabály konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75e9-120">-DefaultProfile</span></span>
<span data-ttu-id="a75e9-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a75e9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a75e9-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="a75e9-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="a75e9-123">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="a75e9-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="a75e9-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a75e9-124">-EnableFloatingIP</span></span>
<span data-ttu-id="a75e9-125">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="a75e9-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a75e9-126">-EnableTcpReset</span></span>
<span data-ttu-id="a75e9-127">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="a75e9-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a75e9-128">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="a75e9-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a75e9-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a75e9-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a75e9-130">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a75e9-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a75e9-132">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a75e9-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a75e9-133">-FrontendPort</span></span>
<span data-ttu-id="a75e9-134">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a75e9-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a75e9-136">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="a75e9-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a75e9-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="a75e9-137">-LoadDistribution</span></span>
<span data-ttu-id="a75e9-138">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-138">Specifies a load distribution.</span></span>
<span data-ttu-id="a75e9-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a75e9-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a75e9-140">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="a75e9-140">Default</span></span>
- <span data-ttu-id="a75e9-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="a75e9-141">SourceIP</span></span>
- <span data-ttu-id="a75e9-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="a75e9-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="a75e9-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a75e9-143">-Name</span></span>
<span data-ttu-id="a75e9-144">A parancsmag által létrehozott terheléselosztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a75e9-145">-Szonda</span><span class="sxs-lookup"><span data-stu-id="a75e9-145">-Probe</span></span>
<span data-ttu-id="a75e9-146">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a75e9-147">-ProbeId</span></span>
<span data-ttu-id="a75e9-148">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="a75e9-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a75e9-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a75e9-149">-Protocol</span></span>
<span data-ttu-id="a75e9-150">A terheléselosztási szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a75e9-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="a75e9-151">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="a75e9-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a75e9-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a75e9-152">-Confirm</span></span>
<span data-ttu-id="a75e9-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a75e9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a75e9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a75e9-154">-WhatIf</span></span>
<span data-ttu-id="a75e9-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a75e9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a75e9-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a75e9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a75e9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75e9-157">CommonParameters</span></span>
<span data-ttu-id="a75e9-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a75e9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75e9-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a75e9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75e9-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a75e9-160">INPUTS</span></span>

### <span data-ttu-id="a75e9-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a75e9-161">System.String</span></span>

### <span data-ttu-id="a75e9-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a75e9-162">System.Int32</span></span>

### <span data-ttu-id="a75e9-163">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a75e9-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="a75e9-164">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a75e9-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="a75e9-165">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="a75e9-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="a75e9-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a75e9-166">OUTPUTS</span></span>

### <span data-ttu-id="a75e9-167">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a75e9-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="a75e9-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a75e9-168">NOTES</span></span>

## <span data-ttu-id="a75e9-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a75e9-169">RELATED LINKS</span></span>

[<span data-ttu-id="a75e9-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a75e9-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a75e9-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a75e9-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a75e9-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a75e9-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a75e9-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a75e9-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


