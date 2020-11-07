---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843618"
---
# <span data-ttu-id="8c62f-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c62f-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="8c62f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c62f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c62f-103">A terheléselosztási szabályok konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="8c62f-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="8c62f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c62f-104">SYNTAX</span></span>

### <span data-ttu-id="8c62f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c62f-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c62f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8c62f-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c62f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c62f-107">DESCRIPTION</span></span>
<span data-ttu-id="8c62f-108">A **set-AzLoadBalancerRuleConfig** parancsmag a terheléselosztási szabályok konfigurációjának állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="8c62f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c62f-109">EXAMPLES</span></span>

### <span data-ttu-id="8c62f-110">Példa 1: terheléselosztási szabály konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="8c62f-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="8c62f-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8c62f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="8c62f-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerRuleConfig-hoz, amely egy NewRule nevű szabályt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="8c62f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="8c62f-113">A harmadik parancs átadja a terheléselosztó **beállítást a set-AzLoadBalancerRuleConfig** , amely az új szabály konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="8c62f-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="8c62f-114">Ne feledje, hogy a konfiguráció nem engedélyezi az előző parancs által engedélyezett lebegő IP-címet.</span><span class="sxs-lookup"><span data-stu-id="8c62f-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="8c62f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c62f-115">PARAMETERS</span></span>

### <span data-ttu-id="8c62f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c62f-116">-BackendAddressPool</span></span>
<span data-ttu-id="8c62f-117">A terheléselosztási szabályokhoz társítani kívánt **BackendAddressPool** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8c62f-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="8c62f-119">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="8c62f-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8c62f-120">-BackendPort</span></span>
<span data-ttu-id="8c62f-121">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c62f-122">-DefaultProfile</span></span>
<span data-ttu-id="8c62f-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c62f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="8c62f-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="8c62f-125">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="8c62f-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8c62f-126">-EnableFloatingIP</span></span>
<span data-ttu-id="8c62f-127">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="8c62f-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c62f-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8c62f-129">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8c62f-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8c62f-131">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-131">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8c62f-132">-FrontendPort</span></span>
<span data-ttu-id="8c62f-133">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8c62f-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8c62f-135">Azt adja meg, hogy hány percen belül maradjon a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="8c62f-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c62f-136">-LoadBalancer</span></span>
<span data-ttu-id="8c62f-137">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-137">Specifies a load balancer.</span></span>
<span data-ttu-id="8c62f-138">Ez a parancsmag a cél állam szabályának konfigurációját adja meg annak a terheléselosztásnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="8c62f-139">-LoadDistribution</span></span>
<span data-ttu-id="8c62f-140">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-140">Specifies a load distribution.</span></span>
<span data-ttu-id="8c62f-141">A paraméter elfogadható értékei a következők: SourceIP és SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="8c62f-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c62f-142">-Name</span></span>
<span data-ttu-id="8c62f-143">A terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-143">Specifies the name of a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-144">-Szonda</span><span class="sxs-lookup"><span data-stu-id="8c62f-144">-Probe</span></span>
<span data-ttu-id="8c62f-145">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="8c62f-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="8c62f-146">-ProbeId</span></span>
<span data-ttu-id="8c62f-147">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="8c62f-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-148">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8c62f-148">-Protocol</span></span>
<span data-ttu-id="8c62f-149">A terheléselosztási szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c62f-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="8c62f-150">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="8c62f-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c62f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c62f-151">CommonParameters</span></span>
<span data-ttu-id="8c62f-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c62f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c62f-153">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c62f-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c62f-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c62f-154">INPUTS</span></span>

### <span data-ttu-id="8c62f-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c62f-155">PSLoadBalancer</span></span>
<span data-ttu-id="8c62f-156">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8c62f-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8c62f-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c62f-157">OUTPUTS</span></span>

### <span data-ttu-id="8c62f-158">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c62f-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8c62f-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c62f-159">NOTES</span></span>

## <span data-ttu-id="8c62f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c62f-160">RELATED LINKS</span></span>

[<span data-ttu-id="8c62f-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c62f-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8c62f-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c62f-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8c62f-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c62f-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8c62f-164">Új – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c62f-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8c62f-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c62f-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


