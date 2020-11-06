---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495899"
---
# <span data-ttu-id="30eb6-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30eb6-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="30eb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="30eb6-103">Szabály-konfigurációt hoz létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="30eb6-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30eb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30eb6-104">SYNTAX</span></span>

### <span data-ttu-id="30eb6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30eb6-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30eb6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="30eb6-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30eb6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="30eb6-107">DESCRIPTION</span></span>
<span data-ttu-id="30eb6-108">A **New-AzureRmLoadBalancerRuleConfig** parancsmag létrehoz egy szabály-konfigurációt az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="30eb6-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="30eb6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="30eb6-109">EXAMPLES</span></span>

### <span data-ttu-id="30eb6-110">1: szabály-konfiguráció létrehozása Azure-terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="30eb6-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="30eb6-111">Az első három parancs a nyilvános IP-címet, az előtér-előnézetet, valamint a szabály konfigurációjának megfelelő szondát tartalmaz a Forth parancsban.</span><span class="sxs-lookup"><span data-stu-id="30eb6-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="30eb6-112">A Forth parancs új szabályt hoz létre, amelynek neve MyLBrule bizonyos előírásokkal.</span><span class="sxs-lookup"><span data-stu-id="30eb6-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="30eb6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30eb6-113">PARAMETERS</span></span>

### <span data-ttu-id="30eb6-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30eb6-114">-BackendAddressPool</span></span>
<span data-ttu-id="30eb6-115">Itt adhatja meg azt a **BackendAddressPool** -objektumot, amellyel társítani szeretné a terheléselosztó szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="30eb6-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="30eb6-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="30eb6-117">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="30eb6-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="30eb6-118">-BackendPort</span></span>
<span data-ttu-id="30eb6-119">A terheléselosztási szabály konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30eb6-120">-DefaultProfile</span></span>
<span data-ttu-id="30eb6-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30eb6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb6-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="30eb6-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="30eb6-123">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="30eb6-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="30eb6-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="30eb6-124">-EnableFloatingIP</span></span>
<span data-ttu-id="30eb6-125">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="30eb6-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="30eb6-126">-EnableTcpReset</span></span>
<span data-ttu-id="30eb6-127">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="30eb6-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="30eb6-128">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="30eb6-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="30eb6-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="30eb6-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="30eb6-130">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="30eb6-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="30eb6-132">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="30eb6-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="30eb6-133">-FrontendPort</span></span>
<span data-ttu-id="30eb6-134">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="30eb6-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="30eb6-136">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="30eb6-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="30eb6-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="30eb6-137">-LoadDistribution</span></span>
<span data-ttu-id="30eb6-138">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-138">Specifies a load distribution.</span></span>
<span data-ttu-id="30eb6-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="30eb6-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30eb6-140">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="30eb6-140">Default</span></span>
- <span data-ttu-id="30eb6-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="30eb6-141">SourceIP</span></span>
- <span data-ttu-id="30eb6-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="30eb6-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="30eb6-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30eb6-143">-Name</span></span>
<span data-ttu-id="30eb6-144">A parancsmag által létrehozott terheléselosztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="30eb6-145">-Szonda</span><span class="sxs-lookup"><span data-stu-id="30eb6-145">-Probe</span></span>
<span data-ttu-id="30eb6-146">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="30eb6-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="30eb6-147">-ProbeId</span></span>
<span data-ttu-id="30eb6-148">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="30eb6-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30eb6-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="30eb6-149">-Protocol</span></span>
<span data-ttu-id="30eb6-150">A terheléselosztási szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="30eb6-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="30eb6-151">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="30eb6-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="30eb6-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30eb6-152">-Confirm</span></span>
<span data-ttu-id="30eb6-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30eb6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30eb6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30eb6-154">-WhatIf</span></span>
<span data-ttu-id="30eb6-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30eb6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30eb6-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30eb6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30eb6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30eb6-157">CommonParameters</span></span>
<span data-ttu-id="30eb6-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30eb6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30eb6-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30eb6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30eb6-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30eb6-160">INPUTS</span></span>

### <span data-ttu-id="30eb6-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="30eb6-161">None</span></span>

## <span data-ttu-id="30eb6-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30eb6-162">OUTPUTS</span></span>

### <span data-ttu-id="30eb6-163">Microsoft. Azure. commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="30eb6-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="30eb6-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30eb6-164">NOTES</span></span>

## <span data-ttu-id="30eb6-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30eb6-165">RELATED LINKS</span></span>

[<span data-ttu-id="30eb6-166">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30eb6-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="30eb6-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30eb6-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="30eb6-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30eb6-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="30eb6-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30eb6-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


