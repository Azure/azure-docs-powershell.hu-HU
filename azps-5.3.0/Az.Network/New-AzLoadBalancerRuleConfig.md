---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470225"
---
# <span data-ttu-id="65659-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65659-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="65659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65659-102">SYNOPSIS</span></span>
<span data-ttu-id="65659-103">Szabálykonfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="65659-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="65659-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65659-104">SYNTAX</span></span>

### <span data-ttu-id="65659-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65659-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65659-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65659-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65659-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65659-107">DESCRIPTION</span></span>
<span data-ttu-id="65659-108">A **New-AzLoadBalancerRuleConfig** parancsmag létrehoz egy szabálykonfigurációt egy Azure-terheléselegyenlő számára.</span><span class="sxs-lookup"><span data-stu-id="65659-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="65659-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65659-109">EXAMPLES</span></span>

### <span data-ttu-id="65659-110">1. példa: Szabálykonfiguráció létrehozása az Azure Load Balancer eszközben</span><span class="sxs-lookup"><span data-stu-id="65659-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="65659-111">Az első három parancs nyilvános IP-címet, előlapot és szabálykonfigurációt állíthat be a oda-vissza parancsban.</span><span class="sxs-lookup"><span data-stu-id="65659-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="65659-112">A "oda" parancs létrehoz egy MyL Minden nevű szabályt bizonyos specifikációkkal.</span><span class="sxs-lookup"><span data-stu-id="65659-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="65659-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65659-113">PARAMETERS</span></span>

### <span data-ttu-id="65659-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="65659-114">-BackendAddressPool</span></span>
<span data-ttu-id="65659-115">Egy **BackendAddressPool** objektumot ad meg, amely terheléselosztási szabály-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="65659-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="65659-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="65659-117">Annak a **BackendAddressPool-objektumnak** az azonosítóját adja meg, amely a terheléselosztási szabály konfigurációjával társítható.</span><span class="sxs-lookup"><span data-stu-id="65659-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="65659-118">-BackendPort</span></span>
<span data-ttu-id="65659-119">A terheléselosztási szabály konfigurációval egyező forgalom háttér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="65659-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65659-120">-DefaultProfile</span></span>
<span data-ttu-id="65659-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65659-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65659-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="65659-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="65659-123">Konfigurálja a SNAT-t a háttérkészletben található virtuális gépekhez úgy, hogy a terheléselosztási szabály előréjében megadott nyilvános IP-címet használják.</span><span class="sxs-lookup"><span data-stu-id="65659-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="65659-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="65659-124">-EnableFloatingIP</span></span>
<span data-ttu-id="65659-125">Azt jelzi, hogy ez a parancsmag lebegő IP-címet tesz lehetővé egy szabálykonfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="65659-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="65659-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="65659-126">-EnableTcpReset</span></span>
<span data-ttu-id="65659-127">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="65659-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="65659-128">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="65659-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="65659-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="65659-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="65659-130">Megadja az előlapi IP-címek listáját, amelyek a terheléselosztási szabály konfigurációját társítják.</span><span class="sxs-lookup"><span data-stu-id="65659-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="65659-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="65659-132">Az előlapi IP-címek konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="65659-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="65659-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="65659-133">-FrontendPort</span></span>
<span data-ttu-id="65659-134">Azt az előlapi portot adja meg, amelyet egy terheléselosztási szabály konfigurációja megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="65659-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="65659-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="65659-136">Azt adja meg percben, hogy a rendszer a terheléselosztásban tartja-e meg a beszélgetések állapotát percekben.</span><span class="sxs-lookup"><span data-stu-id="65659-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="65659-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="65659-137">-LoadDistribution</span></span>
<span data-ttu-id="65659-138">Terheléseloszlást ad meg.</span><span class="sxs-lookup"><span data-stu-id="65659-138">Specifies a load distribution.</span></span>
<span data-ttu-id="65659-139">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="65659-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65659-140">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="65659-140">Default</span></span>
- <span data-ttu-id="65659-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="65659-141">SourceIP</span></span>
- <span data-ttu-id="65659-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="65659-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="65659-143">-Name</span><span class="sxs-lookup"><span data-stu-id="65659-143">-Name</span></span>
<span data-ttu-id="65659-144">A parancsmag által létrehozott terheléselosztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65659-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="65659-145">– Sivad</span><span class="sxs-lookup"><span data-stu-id="65659-145">-Probe</span></span>
<span data-ttu-id="65659-146">Egy terheléselosztási szabály konfigurációját társító adatbázist ad meg.</span><span class="sxs-lookup"><span data-stu-id="65659-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-147">-AzId-et</span><span class="sxs-lookup"><span data-stu-id="65659-147">-ProbeId</span></span>
<span data-ttu-id="65659-148">Megadja annak a konfigurációnak az azonosítóját, amely a terheléselosztási szabály konfigurációjával társítva van.</span><span class="sxs-lookup"><span data-stu-id="65659-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65659-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="65659-149">-Protocol</span></span>
<span data-ttu-id="65659-150">Azt a protokollt adja meg, amelyet egy terheléselosztási szabály konfigurációja megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="65659-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="65659-151">A paraméter elfogadható értékei: Tcp vagy Udp.</span><span class="sxs-lookup"><span data-stu-id="65659-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="65659-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65659-152">-Confirm</span></span>
<span data-ttu-id="65659-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65659-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65659-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65659-154">-WhatIf</span></span>
<span data-ttu-id="65659-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65659-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65659-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65659-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65659-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65659-157">CommonParameters</span></span>
<span data-ttu-id="65659-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65659-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65659-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65659-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65659-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65659-160">INPUTS</span></span>

### <span data-ttu-id="65659-161">System.String</span><span class="sxs-lookup"><span data-stu-id="65659-161">System.String</span></span>

### <span data-ttu-id="65659-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="65659-162">System.Int32</span></span>

### <span data-ttu-id="65659-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65659-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="65659-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="65659-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="65659-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="65659-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="65659-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65659-166">OUTPUTS</span></span>

### <span data-ttu-id="65659-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="65659-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="65659-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65659-168">NOTES</span></span>

## <span data-ttu-id="65659-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65659-169">RELATED LINKS</span></span>

[<span data-ttu-id="65659-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65659-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="65659-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65659-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="65659-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65659-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="65659-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65659-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


