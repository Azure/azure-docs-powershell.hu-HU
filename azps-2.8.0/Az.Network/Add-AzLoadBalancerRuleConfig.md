---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: e6df07d9d3f133390c6c6d14e092e7983324f753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837664"
---
# <span data-ttu-id="72249-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72249-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="72249-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72249-102">SYNOPSIS</span></span>
<span data-ttu-id="72249-103">Egy szabály-konfigurációt ad hozzá a terheléselosztó bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="72249-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="72249-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72249-104">SYNTAX</span></span>

### <span data-ttu-id="72249-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72249-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72249-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72249-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72249-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72249-107">DESCRIPTION</span></span>
<span data-ttu-id="72249-108">Az **Add-AzLoadBalancerRuleConfig** parancsmag egy szabály-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="72249-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="72249-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72249-109">EXAMPLES</span></span>

### <span data-ttu-id="72249-110">1. példa: szabály-konfiguráció hozzáadása a terheléselosztó bővítményhez</span><span class="sxs-lookup"><span data-stu-id="72249-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="72249-111">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="72249-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="72249-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb **-AzLoadBalancerRuleConfig** , amely hozzáadja a NewRule nevű szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="72249-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="72249-113">A harmadik parancs az Azure-ban az új terheléselosztó szabály konfigurációval frissíti az Azure-t.</span><span class="sxs-lookup"><span data-stu-id="72249-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="72249-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72249-114">PARAMETERS</span></span>

### <span data-ttu-id="72249-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72249-115">-BackendAddressPool</span></span>
<span data-ttu-id="72249-116">Annak a backend-címkészletet adja meg, amely a terheléselosztó szabály konfigurációjával van társítva.</span><span class="sxs-lookup"><span data-stu-id="72249-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="72249-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="72249-118">Annak a **BackendAddressPool** -objektumnak az azonosítóját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="72249-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="72249-119">-BackendPort</span></span>
<span data-ttu-id="72249-120">A terheléselosztási szabályok konfigurációjának megfelelő adatforgalomhoz tartozó backend-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72249-121">-DefaultProfile</span></span>
<span data-ttu-id="72249-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72249-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72249-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="72249-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="72249-124">Beállítja a SNAT a VMs-rendszerhez a backend-készletben, hogy a terheléselosztási szabály publicIP megadott címet használja.</span><span class="sxs-lookup"><span data-stu-id="72249-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="72249-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="72249-125">-EnableFloatingIP</span></span>
<span data-ttu-id="72249-126">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="72249-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="72249-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="72249-127">-EnableTcpReset</span></span>
<span data-ttu-id="72249-128">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="72249-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="72249-129">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="72249-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="72249-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="72249-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="72249-131">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="72249-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="72249-133">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="72249-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="72249-134">-FrontendPort</span></span>
<span data-ttu-id="72249-135">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="72249-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="72249-137">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztó lapon.</span><span class="sxs-lookup"><span data-stu-id="72249-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="72249-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72249-138">-LoadBalancer</span></span>
<span data-ttu-id="72249-139">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="72249-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="72249-140">Ez a parancsmag egy szabály-konfigurációt szúr be a paraméter által megadott terheléselosztó értékhez.</span><span class="sxs-lookup"><span data-stu-id="72249-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="72249-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="72249-141">-LoadDistribution</span></span>
<span data-ttu-id="72249-142">A betöltő eloszlását adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="72249-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72249-143">-Name</span></span>
<span data-ttu-id="72249-144">A terheléselosztó szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-145">-Szonda</span><span class="sxs-lookup"><span data-stu-id="72249-145">-Probe</span></span>
<span data-ttu-id="72249-146">Itt adhatja meg azt a szondát, amellyel társítani lehet egy terheléselosztó szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="72249-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="72249-147">-ProbeId</span></span>
<span data-ttu-id="72249-148">Annak a szondanak az AZONOSÍTÓját adja meg, amelyet a terheléselosztó szabály konfigurációjával társíthat.</span><span class="sxs-lookup"><span data-stu-id="72249-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72249-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="72249-149">-Protocol</span></span>
<span data-ttu-id="72249-150">A terheléselosztási szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="72249-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="72249-151">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="72249-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="72249-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72249-152">-Confirm</span></span>
<span data-ttu-id="72249-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72249-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72249-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72249-154">-WhatIf</span></span>
<span data-ttu-id="72249-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72249-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72249-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72249-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72249-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72249-157">CommonParameters</span></span>
<span data-ttu-id="72249-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72249-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72249-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72249-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72249-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72249-160">INPUTS</span></span>

### <span data-ttu-id="72249-161">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72249-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="72249-162">System. String</span><span class="sxs-lookup"><span data-stu-id="72249-162">System.String</span></span>

### <span data-ttu-id="72249-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="72249-163">System.Int32</span></span>

### <span data-ttu-id="72249-164">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="72249-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="72249-165">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72249-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="72249-166">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="72249-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="72249-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72249-167">OUTPUTS</span></span>

### <span data-ttu-id="72249-168">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72249-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="72249-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72249-169">NOTES</span></span>

## <span data-ttu-id="72249-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72249-170">RELATED LINKS</span></span>

[<span data-ttu-id="72249-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72249-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="72249-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72249-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="72249-173">Új – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72249-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="72249-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72249-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="72249-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72249-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


