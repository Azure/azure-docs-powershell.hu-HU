---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ea27d5b58586aeb9e627c926fc67d89cfe8ec354
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670006"
---
# <span data-ttu-id="fe601-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe601-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="fe601-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe601-102">SYNOPSIS</span></span>
<span data-ttu-id="fe601-103">Bejövő hálózati címfordítási szabály konfigurációjának beállítása terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="fe601-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="fe601-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe601-104">SYNTAX</span></span>

### <span data-ttu-id="fe601-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe601-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe601-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe601-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe601-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe601-107">DESCRIPTION</span></span>
<span data-ttu-id="fe601-108">A **set-AzLoadBalancerInboundNatRuleConfig** parancsmag egy beérkező hálózati címfordítási (NAT) szabály-konfigurációt állít be egy Azure-terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="fe601-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="fe601-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fe601-109">EXAMPLES</span></span>

### <span data-ttu-id="fe601-110">Példa 1: a bejövő CÍMFORDÍTÁSi szabály konfigurációjának módosítása a terheléselosztó eszközön</span><span class="sxs-lookup"><span data-stu-id="fe601-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="fe601-111">Az első parancs megkapja a MyLoadBalancer nevű terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe601-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="fe601-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a AzLoadBalancerInboundNatRuleConfig-hoz, ami beérkező hálózati címfordítási szabály konfigurációját adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="fe601-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="fe601-113">A harmadik parancs átadja a kiegyenlítőt a **set-AzLoadBalancerInboundNatRuleConfig** , amely menti és FRISSÍTI a NAT-szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="fe601-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="fe601-114">Fontos tudni, hogy a szabály konfigurációja a lebegő IP engedélyezése nélkül volt beállítva, amelyet az előző parancs engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="fe601-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="fe601-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe601-115">PARAMETERS</span></span>

### <span data-ttu-id="fe601-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fe601-116">-BackendPort</span></span>
<span data-ttu-id="fe601-117">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="fe601-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe601-118">-DefaultProfile</span></span>
<span data-ttu-id="fe601-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe601-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe601-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="fe601-120">-EnableFloatingIP</span></span>
<span data-ttu-id="fe601-121">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="fe601-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="fe601-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="fe601-122">-EnableTcpReset</span></span>
<span data-ttu-id="fe601-123">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="fe601-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="fe601-124">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="fe601-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="fe601-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe601-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="fe601-126">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="fe601-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fe601-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="fe601-128">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="fe601-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="fe601-129">-FrontendPort</span></span>
<span data-ttu-id="fe601-130">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fe601-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fe601-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fe601-132">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="fe601-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="fe601-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fe601-133">-LoadBalancer</span></span>
<span data-ttu-id="fe601-134">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-134">Specifies a load balancer.</span></span>
<span data-ttu-id="fe601-135">Ez a parancsmag bejelöli a hálózati címfordítási szabály konfigurációját a paraméter által megadott terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="fe601-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe601-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe601-136">-Name</span></span>
<span data-ttu-id="fe601-137">A beérkező NAT-szabályok konfigurációjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="fe601-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="fe601-138">-Protocol</span></span>
<span data-ttu-id="fe601-139">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjának megfelelő protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe601-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="fe601-140">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="fe601-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="fe601-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe601-141">-Confirm</span></span>
<span data-ttu-id="fe601-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe601-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe601-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe601-143">-WhatIf</span></span>
<span data-ttu-id="fe601-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe601-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe601-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe601-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe601-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe601-146">CommonParameters</span></span>
<span data-ttu-id="fe601-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe601-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe601-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe601-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe601-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe601-149">INPUTS</span></span>

### <span data-ttu-id="fe601-150">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fe601-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="fe601-151">System. String</span><span class="sxs-lookup"><span data-stu-id="fe601-151">System.String</span></span>

### <span data-ttu-id="fe601-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fe601-152">System.Int32</span></span>

### <span data-ttu-id="fe601-153">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe601-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="fe601-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe601-154">OUTPUTS</span></span>

### <span data-ttu-id="fe601-155">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fe601-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fe601-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe601-156">NOTES</span></span>

## <span data-ttu-id="fe601-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe601-157">RELATED LINKS</span></span>

[<span data-ttu-id="fe601-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe601-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fe601-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fe601-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="fe601-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe601-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fe601-161">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe601-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fe601-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe601-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


