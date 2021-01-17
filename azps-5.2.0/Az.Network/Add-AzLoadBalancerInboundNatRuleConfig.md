---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365593"
---
# <span data-ttu-id="b4f8b-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4f8b-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b4f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f8b-103">Bejövő NAT-szabálykonfigurációt ad a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="b4f8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b4f8b-104">SYNTAX</span></span>

### <span data-ttu-id="b4f8b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4f8b-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f8b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f8b-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f8b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b4f8b-107">DESCRIPTION</span></span>
<span data-ttu-id="b4f8b-108">Az **Add-AzLoadBalancerInboundNatRuleConfig** parancsmag egy bejövő hálózati címfordítási (NAT) szabálykonfigurációt ad az Azure terheléselegyenlőjénél.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b4f8b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b4f8b-109">EXAMPLES</span></span>

### <span data-ttu-id="b4f8b-110">1. példa: Bejövő NAT-szabály konfigurációjának hozzáadása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="b4f8b-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="b4f8b-111">Az első parancs lejátsa a MyloadBalancer nevű terheléselosztási $slb.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b4f8b-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az **Add-AzLoadBalancerInboundNatRuleConfig** szolgáltatónak, amely bejövő NAT-szabálykonfigurációt ad a terheléselegyenlítóhoz.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="b4f8b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4f8b-113">PARAMETERS</span></span>

### <span data-ttu-id="b4f8b-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b4f8b-114">-BackendPort</span></span>
<span data-ttu-id="b4f8b-115">Egy szabálykonfigurációval egyező forgalom háttér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b4f8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f8b-116">-DefaultProfile</span></span>
<span data-ttu-id="b4f8b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4f8b-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b4f8b-118">-EnableFloatingIP</span></span>
<span data-ttu-id="b4f8b-119">Azt jelzi, hogy ez a parancsmag lebegő IP-címet tesz lehetővé egy szabálykonfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b4f8b-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b4f8b-120">-EnableTcpReset</span></span>
<span data-ttu-id="b4f8b-121">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b4f8b-122">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b4f8b-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4f8b-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b4f8b-124">Megadja az előlapi IP-címek listáját, amelyek bejövő NAT-szabálykonfigurációval társítva vannak.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b4f8b-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4f8b-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b4f8b-126">Az előlapi IP-címek konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b4f8b-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b4f8b-127">-FrontendPort</span></span>
<span data-ttu-id="b4f8b-128">Meghatározza a szabálykonfigurációval egyező előlapi portot.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b4f8b-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b4f8b-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b4f8b-130">Azt adja meg percben, hogy a rendszer a terheléselosztásban tartja-e meg a beszélgetések állapotát percekben.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b4f8b-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f8b-131">-LoadBalancer</span></span>
<span data-ttu-id="b4f8b-132">Egy **LoadBalancer-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b4f8b-133">Ez a parancsmag egy bejövő NAT-szabálykonfigurációt ad a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4f8b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b4f8b-134">-Name</span></span>
<span data-ttu-id="b4f8b-135">Megadja a hozzáadni szükséges bejövő NAT-szabály konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="b4f8b-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b4f8b-136">-Protocol</span></span>
<span data-ttu-id="b4f8b-137">Azt a protokollt adja meg, amelyet egy bejövő NAT-szabály megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="b4f8b-138">A paraméter elfogadható értékei: Tcp vagy Udp.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b4f8b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4f8b-139">-Confirm</span></span>
<span data-ttu-id="b4f8b-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f8b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f8b-141">-WhatIf</span></span>
<span data-ttu-id="b4f8b-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4f8b-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f8b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f8b-144">CommonParameters</span></span>
<span data-ttu-id="b4f8b-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f8b-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f8b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f8b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4f8b-147">INPUTS</span></span>

### <span data-ttu-id="b4f8b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f8b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b4f8b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b4f8b-149">System.String</span></span>

### <span data-ttu-id="b4f8b-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b4f8b-150">System.Int32</span></span>

### <span data-ttu-id="b4f8b-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4f8b-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b4f8b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f8b-152">OUTPUTS</span></span>

### <span data-ttu-id="b4f8b-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f8b-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b4f8b-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b4f8b-154">NOTES</span></span>

## <span data-ttu-id="b4f8b-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4f8b-155">RELATED LINKS</span></span>

[<span data-ttu-id="b4f8b-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f8b-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b4f8b-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4f8b-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b4f8b-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4f8b-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b4f8b-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4f8b-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b4f8b-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4f8b-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="b4f8b-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4f8b-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


