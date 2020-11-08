---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181610"
---
# <span data-ttu-id="ddbe2-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddbe2-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ddbe2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbe2-103">Bejövő NAT-szabályok konfigurációjának hozzáadása a terheléselosztó eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="ddbe2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddbe2-104">SYNTAX</span></span>

### <span data-ttu-id="ddbe2-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ddbe2-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddbe2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddbe2-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddbe2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddbe2-107">DESCRIPTION</span></span>
<span data-ttu-id="ddbe2-108">Az **Add-AzLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt ad hozzá az Azure terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="ddbe2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ddbe2-109">EXAMPLES</span></span>

### <span data-ttu-id="ddbe2-110">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának hozzáadása a terheléselosztó eszközhöz</span><span class="sxs-lookup"><span data-stu-id="ddbe2-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="ddbe2-111">Az első parancs beolvassa a MyloadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ddbe2-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a **AzLoadBalancerInboundNatRuleConfig-** hoz, ami beszámítja a beérkező NAT-szabályok konfigurációját a terheléselosztásba.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="ddbe2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddbe2-113">PARAMETERS</span></span>

### <span data-ttu-id="ddbe2-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ddbe2-114">-BackendPort</span></span>
<span data-ttu-id="ddbe2-115">A szabály-konfigurációval kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="ddbe2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbe2-116">-DefaultProfile</span></span>
<span data-ttu-id="ddbe2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddbe2-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ddbe2-118">-EnableFloatingIP</span></span>
<span data-ttu-id="ddbe2-119">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ddbe2-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ddbe2-120">-EnableTcpReset</span></span>
<span data-ttu-id="ddbe2-121">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="ddbe2-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ddbe2-122">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ddbe2-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddbe2-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ddbe2-124">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ddbe2-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ddbe2-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ddbe2-126">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ddbe2-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ddbe2-127">-FrontendPort</span></span>
<span data-ttu-id="ddbe2-128">A szabály-konfigurációval egyező előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="ddbe2-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ddbe2-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ddbe2-130">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ddbe2-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddbe2-131">-LoadBalancer</span></span>
<span data-ttu-id="ddbe2-132">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="ddbe2-133">Ez a parancsmag a bejövő NAT-szabályok konfigurációját hozzáadja a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddbe2-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddbe2-134">-Name</span></span>
<span data-ttu-id="ddbe2-135">Itt adhatja meg a hozzáadni kívánt bejövő CÍMFORDÍTÁSi szabály konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="ddbe2-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ddbe2-136">-Protocol</span></span>
<span data-ttu-id="ddbe2-137">A bejövő CÍMFORDÍTÁSi szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="ddbe2-138">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ddbe2-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddbe2-139">-Confirm</span></span>
<span data-ttu-id="ddbe2-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbe2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbe2-141">-WhatIf</span></span>
<span data-ttu-id="ddbe2-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddbe2-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddbe2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbe2-144">CommonParameters</span></span>
<span data-ttu-id="ddbe2-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddbe2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbe2-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbe2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbe2-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddbe2-147">INPUTS</span></span>

### <span data-ttu-id="ddbe2-148">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddbe2-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ddbe2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ddbe2-149">System.String</span></span>

### <span data-ttu-id="ddbe2-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ddbe2-150">System.Int32</span></span>

### <span data-ttu-id="ddbe2-151">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddbe2-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ddbe2-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddbe2-152">OUTPUTS</span></span>

### <span data-ttu-id="ddbe2-153">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddbe2-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ddbe2-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddbe2-154">NOTES</span></span>

## <span data-ttu-id="ddbe2-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddbe2-155">RELATED LINKS</span></span>

[<span data-ttu-id="ddbe2-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddbe2-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ddbe2-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddbe2-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ddbe2-158">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddbe2-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ddbe2-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddbe2-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ddbe2-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddbe2-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="ddbe2-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddbe2-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


