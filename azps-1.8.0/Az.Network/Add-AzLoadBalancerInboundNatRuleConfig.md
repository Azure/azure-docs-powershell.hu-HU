---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 1cfee59f1432cee5355ae562f8cc732a640d8c2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670707"
---
# <span data-ttu-id="0c71d-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c71d-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="0c71d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c71d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c71d-103">Bejövő NAT-szabályok konfigurációjának hozzáadása a terheléselosztó eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="0c71d-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="0c71d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c71d-104">SYNTAX</span></span>

### <span data-ttu-id="0c71d-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c71d-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c71d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c71d-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c71d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c71d-107">DESCRIPTION</span></span>
<span data-ttu-id="0c71d-108">Az **Add-AzLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabály-konfigurációt ad hozzá az Azure terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="0c71d-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0c71d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0c71d-109">EXAMPLES</span></span>

### <span data-ttu-id="0c71d-110">1. példa: bejövő CÍMFORDÍTÁSi szabály konfigurációjának hozzáadása a terheléselosztó eszközhöz</span><span class="sxs-lookup"><span data-stu-id="0c71d-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="0c71d-111">Az első parancs beolvassa a MyloadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="0c71d-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0c71d-112">A második parancs a pipeline operátor segítségével továbbítja a terheléselosztást $slb a **AzLoadBalancerInboundNatRuleConfig-** hoz, ami beszámítja a beérkező NAT-szabályok konfigurációját a terheléselosztásba.</span><span class="sxs-lookup"><span data-stu-id="0c71d-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="0c71d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c71d-113">PARAMETERS</span></span>

### <span data-ttu-id="0c71d-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0c71d-114">-BackendPort</span></span>
<span data-ttu-id="0c71d-115">A szabály-konfigurációval kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c71d-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="0c71d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c71d-116">-DefaultProfile</span></span>
<span data-ttu-id="0c71d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c71d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c71d-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0c71d-118">-EnableFloatingIP</span></span>
<span data-ttu-id="0c71d-119">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="0c71d-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0c71d-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0c71d-120">-EnableTcpReset</span></span>
<span data-ttu-id="0c71d-121">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="0c71d-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0c71d-122">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="0c71d-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0c71d-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c71d-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0c71d-124">A bejövő CÍMFORDÍTÁSi szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c71d-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="0c71d-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0c71d-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0c71d-126">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c71d-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0c71d-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0c71d-127">-FrontendPort</span></span>
<span data-ttu-id="0c71d-128">A szabály-konfigurációval egyező előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c71d-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="0c71d-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0c71d-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0c71d-130">Azt adja meg, hogy hány perc múlva maradjon meg a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="0c71d-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="0c71d-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c71d-131">-LoadBalancer</span></span>
<span data-ttu-id="0c71d-132">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0c71d-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="0c71d-133">Ez a parancsmag a bejövő NAT-szabályok konfigurációját hozzáadja a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="0c71d-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c71d-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c71d-134">-Name</span></span>
<span data-ttu-id="0c71d-135">Itt adhatja meg a hozzáadni kívánt bejövő CÍMFORDÍTÁSi szabály konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="0c71d-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="0c71d-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0c71d-136">-Protocol</span></span>
<span data-ttu-id="0c71d-137">A bejövő CÍMFORDÍTÁSi szabályok által egyeztetett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c71d-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="0c71d-138">A paraméter elfogadható értékei a következők: TCP vagy UDP.</span><span class="sxs-lookup"><span data-stu-id="0c71d-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="0c71d-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c71d-139">-Confirm</span></span>
<span data-ttu-id="0c71d-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c71d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c71d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c71d-141">-WhatIf</span></span>
<span data-ttu-id="0c71d-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c71d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c71d-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c71d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c71d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c71d-144">CommonParameters</span></span>
<span data-ttu-id="0c71d-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c71d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c71d-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c71d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c71d-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c71d-147">INPUTS</span></span>

### <span data-ttu-id="0c71d-148">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c71d-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0c71d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0c71d-149">System.String</span></span>

### <span data-ttu-id="0c71d-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0c71d-150">System.Int32</span></span>

### <span data-ttu-id="0c71d-151">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c71d-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="0c71d-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c71d-152">OUTPUTS</span></span>

### <span data-ttu-id="0c71d-153">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c71d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0c71d-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c71d-154">NOTES</span></span>

## <span data-ttu-id="0c71d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c71d-155">RELATED LINKS</span></span>

[<span data-ttu-id="0c71d-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c71d-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0c71d-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c71d-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0c71d-158">Új – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c71d-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0c71d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c71d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0c71d-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c71d-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="0c71d-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c71d-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


