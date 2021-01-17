---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467466"
---
# <span data-ttu-id="7b981-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b981-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7b981-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b981-102">SYNOPSIS</span></span>
<span data-ttu-id="7b981-103">Szabálykonfigurációt ad a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="7b981-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="7b981-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b981-104">SYNTAX</span></span>

### <span data-ttu-id="7b981-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b981-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b981-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b981-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b981-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b981-107">DESCRIPTION</span></span>
<span data-ttu-id="7b981-108">Az **Add-AzLoadBalancerRuleConfig** parancsmag hozzáad egy szabálykonfigurációt az Azure terheléselegyenlőjénél.</span><span class="sxs-lookup"><span data-stu-id="7b981-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7b981-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b981-109">EXAMPLES</span></span>

### <span data-ttu-id="7b981-110">1. példa: Szabálykonfiguráció hozzáadása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="7b981-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="7b981-111">Az első parancs lejátsa a MyLoadBalancer nevű terheléselosztási törlőt, majd tárolja azt a $slb.</span><span class="sxs-lookup"><span data-stu-id="7b981-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="7b981-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az **Add-AzLoadBalancerRuleConfig** bővítménynek, amely hozzáadja a NewRule nevű szabálykonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7b981-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="7b981-113">A harmadik parancs frissíti a terheléselegyenlőt az Azure-ban az új Load Balancer rule config segítségével.</span><span class="sxs-lookup"><span data-stu-id="7b981-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="7b981-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b981-114">PARAMETERS</span></span>

### <span data-ttu-id="7b981-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b981-115">-BackendAddressPool</span></span>
<span data-ttu-id="7b981-116">Megadja a háttércímkészletet, amely a terheléselosztási szabály konfigurációját társítja.</span><span class="sxs-lookup"><span data-stu-id="7b981-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7b981-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="7b981-118">Annak a **BackendAddressPool-objektumnak** az azonosítóját adja meg, amely a terheléselosztási szabály konfigurációjával társítható.</span><span class="sxs-lookup"><span data-stu-id="7b981-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7b981-119">-BackendPort</span></span>
<span data-ttu-id="7b981-120">A terheléselosztási szabály konfigurációval egyező forgalom háttér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b981-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b981-121">-DefaultProfile</span></span>
<span data-ttu-id="7b981-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b981-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b981-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="7b981-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="7b981-124">Konfigurálja a SNAT-t a háttérkészletben található virtuális gépekhez úgy, hogy a terheléselosztási szabály előréjében megadott nyilvános IP-címet használják.</span><span class="sxs-lookup"><span data-stu-id="7b981-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="7b981-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7b981-125">-EnableFloatingIP</span></span>
<span data-ttu-id="7b981-126">Azt jelzi, hogy ez a parancsmag lebegő IP-címet tesz lehetővé egy szabálykonfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="7b981-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7b981-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7b981-127">-EnableTcpReset</span></span>
<span data-ttu-id="7b981-128">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="7b981-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7b981-129">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="7b981-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7b981-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b981-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7b981-131">Megadja az előlapi IP-címek listáját, amelyek a terheléselosztási szabály konfigurációját társítják.</span><span class="sxs-lookup"><span data-stu-id="7b981-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7b981-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7b981-133">Az előlapi IP-címek konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b981-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7b981-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7b981-134">-FrontendPort</span></span>
<span data-ttu-id="7b981-135">Azt az előlapi portot adja meg, amelyet egy terheléselosztási szabály konfigurációja megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="7b981-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b981-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7b981-137">Azt adja meg percben, hogy a rendszer a terheléselosztásban tartja-e meg a beszélgetések állapotát percekben.</span><span class="sxs-lookup"><span data-stu-id="7b981-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="7b981-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b981-138">-LoadBalancer</span></span>
<span data-ttu-id="7b981-139">Egy **LoadBalancer-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="7b981-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7b981-140">Ez a parancsmag hozzáadja a paraméter által megadott szabálykonfigurációt a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="7b981-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b981-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="7b981-141">-LoadDistribution</span></span>
<span data-ttu-id="7b981-142">Terheléseloszlást ad meg.</span><span class="sxs-lookup"><span data-stu-id="7b981-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="7b981-143">-Name</span><span class="sxs-lookup"><span data-stu-id="7b981-143">-Name</span></span>
<span data-ttu-id="7b981-144">A terheléselosztási szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b981-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-145">– Sivad</span><span class="sxs-lookup"><span data-stu-id="7b981-145">-Probe</span></span>
<span data-ttu-id="7b981-146">Egy terheléselosztási szabály konfigurációját társító adatbázist ad meg.</span><span class="sxs-lookup"><span data-stu-id="7b981-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-147">-AzId-et</span><span class="sxs-lookup"><span data-stu-id="7b981-147">-ProbeId</span></span>
<span data-ttu-id="7b981-148">Megadja annak a konfigurációnak az azonosítóját, amely a terheléselosztási szabály konfigurációjával társítva van.</span><span class="sxs-lookup"><span data-stu-id="7b981-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b981-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7b981-149">-Protocol</span></span>
<span data-ttu-id="7b981-150">Azt a protokollt adja meg, amelyet egy terheléselosztási szabály megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="7b981-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="7b981-151">A paraméter elfogadható értékei: Tcp vagy Udp.</span><span class="sxs-lookup"><span data-stu-id="7b981-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7b981-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b981-152">-Confirm</span></span>
<span data-ttu-id="7b981-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b981-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b981-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b981-154">-WhatIf</span></span>
<span data-ttu-id="7b981-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b981-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b981-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b981-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b981-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b981-157">CommonParameters</span></span>
<span data-ttu-id="7b981-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b981-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b981-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b981-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b981-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b981-160">INPUTS</span></span>

### <span data-ttu-id="7b981-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b981-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7b981-162">System.String</span><span class="sxs-lookup"><span data-stu-id="7b981-162">System.String</span></span>

### <span data-ttu-id="7b981-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7b981-163">System.Int32</span></span>

### <span data-ttu-id="7b981-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b981-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="7b981-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b981-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="7b981-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="7b981-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="7b981-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b981-167">OUTPUTS</span></span>

### <span data-ttu-id="7b981-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b981-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7b981-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b981-169">NOTES</span></span>

## <span data-ttu-id="7b981-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b981-170">RELATED LINKS</span></span>

[<span data-ttu-id="7b981-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b981-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7b981-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b981-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7b981-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b981-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7b981-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b981-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7b981-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b981-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


