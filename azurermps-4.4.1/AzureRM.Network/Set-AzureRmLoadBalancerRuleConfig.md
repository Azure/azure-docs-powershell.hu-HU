---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 2b9c835e99a088a075656cd985004663e5ef094a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494811"
---
# <span data-ttu-id="dd9d0-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd9d0-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="dd9d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9d0-103">A terheléselosztási szabályok konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd9d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd9d0-104">SYNTAX</span></span>

### <span data-ttu-id="dd9d0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd9d0-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd9d0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dd9d0-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd9d0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd9d0-107">DESCRIPTION</span></span>
<span data-ttu-id="dd9d0-108">A **set-AzureRmLoadBalancerRuleConfig** parancsmag a terheléselosztási szabályok konfigurációjának állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="dd9d0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd9d0-109">EXAMPLES</span></span>

### <span data-ttu-id="dd9d0-110">Példa 1: terheléselosztási szabály konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="dd9d0-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="dd9d0-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="dd9d0-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzureRmLoadBalancerRuleConfig-hoz, amely egy NewRule nevű szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="dd9d0-113">A harmadik parancs átadja a terheléselosztó **beállítást a set-AzureRmLoadBalancerRuleConfig** , amely az új szabály konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="dd9d0-114">Ne feledje, hogy a konfiguráció nem engedélyezi az előző parancs által engedélyezett lebegő IP-címet.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="dd9d0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd9d0-115">PARAMETERS</span></span>

### <span data-ttu-id="dd9d0-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dd9d0-116">-BackendAddressPool</span></span>
<span data-ttu-id="dd9d0-117">A terheléselosztási szabályokhoz társítani kívánt **BackendAddressPool** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="dd9d0-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="dd9d0-119">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="dd9d0-120">-BackendPort</span></span>
<span data-ttu-id="dd9d0-121">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="dd9d0-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="dd9d0-123">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="dd9d0-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="dd9d0-124">-EnableFloatingIP</span></span>
<span data-ttu-id="dd9d0-125">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="dd9d0-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd9d0-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="dd9d0-127">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dd9d0-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="dd9d0-129">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="dd9d0-130">-FrontendPort</span></span>
<span data-ttu-id="dd9d0-131">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd9d0-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dd9d0-133">Azt adja meg, hogy hány percen belül maradjon a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dd9d0-134">-LoadBalancer</span></span>
<span data-ttu-id="dd9d0-135">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-135">Specifies a load balancer.</span></span>
<span data-ttu-id="dd9d0-136">Ez a parancsmag a cél állam szabályának konfigurációját adja meg annak a terheléselosztásnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-136">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="dd9d0-137">-LoadDistribution</span></span>
<span data-ttu-id="dd9d0-138">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-138">Specifies a load distribution.</span></span>
<span data-ttu-id="dd9d0-139">A paraméter elfogadható értékei a következők: SourceIP és SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-139">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd9d0-140">-Name</span></span>
<span data-ttu-id="dd9d0-141">A terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-141">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="dd9d0-142">-Szonda</span><span class="sxs-lookup"><span data-stu-id="dd9d0-142">-Probe</span></span>
<span data-ttu-id="dd9d0-143">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="dd9d0-144">-ProbeId</span></span>
<span data-ttu-id="dd9d0-145">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="dd9d0-146">-Protocol</span></span>
<span data-ttu-id="dd9d0-147">A terheléselosztási szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-147">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="dd9d0-148">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d0-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9d0-149">-DefaultProfile</span></span>
<span data-ttu-id="dd9d0-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd9d0-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd9d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9d0-151">CommonParameters</span></span>
<span data-ttu-id="dd9d0-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd9d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9d0-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd9d0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9d0-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd9d0-154">INPUTS</span></span>

### <span data-ttu-id="dd9d0-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dd9d0-155">PSLoadBalancer</span></span>
<span data-ttu-id="dd9d0-156">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dd9d0-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dd9d0-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd9d0-157">OUTPUTS</span></span>

### <span data-ttu-id="dd9d0-158">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dd9d0-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dd9d0-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd9d0-159">NOTES</span></span>

## <span data-ttu-id="dd9d0-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd9d0-160">RELATED LINKS</span></span>

[<span data-ttu-id="dd9d0-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd9d0-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dd9d0-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd9d0-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dd9d0-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd9d0-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dd9d0-164">Új – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd9d0-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dd9d0-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd9d0-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


