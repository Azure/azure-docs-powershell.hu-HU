---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481140"
---
# <span data-ttu-id="ef7a4-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7a4-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ef7a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7a4-103">Bejövő NAT-szabálykonfigurációt állít be a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ef7a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef7a4-104">SYNTAX</span></span>

### <span data-ttu-id="ef7a4-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef7a4-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef7a4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef7a4-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7a4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef7a4-107">DESCRIPTION</span></span>
<span data-ttu-id="ef7a4-108">A **Set-AzLoadBalancerInboundNatRuleConfig** parancsmag bejövő hálózati címfordítási (NAT) szabálykonfigurációt állít be egy Azure terheléselegyenlítóhoz.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ef7a4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef7a4-109">EXAMPLES</span></span>

### <span data-ttu-id="ef7a4-110">1. példa: A bejövő NAT-szabály konfigurációjának módosítása terheléselosztáskor</span><span class="sxs-lookup"><span data-stu-id="ef7a4-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="ef7a4-111">Az első parancs lekérte a MyLoadBalancer nevű terheléselosztási törlőt, majd a $slb tárolja.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="ef7a4-112">A második parancs a folyamat műveleti jelével adja át a $slb terheléselegyenlőt az Add-AzLoadBalancerInboundNatRuleConfig szolgáltatónak, amely bejövő NAT-szabálykonfigurációt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="ef7a4-113">A harmadik parancs átadja a terheléselegyenlőt a **Set-AzLoadBalancerInboundNatRuleConfig** parancsnak, amely menti és frissíti a bejövő NAT-szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="ef7a4-114">Ne feledje, hogy a szabálykonfiguráció a lebegő IP-címek engedélyezése nélkül lett beállítva, amelyet az előző parancs engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="ef7a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef7a4-115">PARAMETERS</span></span>

### <span data-ttu-id="ef7a4-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ef7a4-116">-BackendPort</span></span>
<span data-ttu-id="ef7a4-117">Az ezzel a szabálykonfigurációval egyező forgalom háttér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="ef7a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7a4-118">-DefaultProfile</span></span>
<span data-ttu-id="ef7a4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7a4-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ef7a4-120">-EnableFloatingIP</span></span>
<span data-ttu-id="ef7a4-121">Azt jelzi, hogy ez a parancsmag lebegő IP-címet tesz lehetővé egy szabálykonfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ef7a4-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ef7a4-122">-EnableTcpReset</span></span>
<span data-ttu-id="ef7a4-123">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ef7a4-124">Ez az elem csak AKKOR használatos, ha a protokoll TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ef7a4-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef7a4-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ef7a4-126">Megadja az előlapi IP-címek listáját, amelyek bejövő NAT-szabálykonfigurációval társítva vannak.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ef7a4-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ef7a4-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ef7a4-128">Az előlapi IP-címek konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ef7a4-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ef7a4-129">-FrontendPort</span></span>
<span data-ttu-id="ef7a4-130">Azt az előlapi portot adja meg, amelyet egy terheléselosztási szabály konfigurációja megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ef7a4-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef7a4-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ef7a4-132">Azt adja meg percben, hogy a rendszer a terheléselosztásban tartja-e meg a beszélgetések állapotát percekben.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ef7a4-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef7a4-133">-LoadBalancer</span></span>
<span data-ttu-id="ef7a4-134">Terheléselosztást ad meg.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-134">Specifies a load balancer.</span></span>
<span data-ttu-id="ef7a4-135">Ez a parancsmag bejövő NAT-szabálykonfigurációt állít be a paraméter által megadott terhelésegyenleg-elosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef7a4-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ef7a4-136">-Name</span></span>
<span data-ttu-id="ef7a4-137">Egy bejövő NAT-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ef7a4-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ef7a4-138">-Protocol</span></span>
<span data-ttu-id="ef7a4-139">Azt a protokollt adja meg, amely megfelel egy bejövő NAT-szabály konfigurációjának.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="ef7a4-140">A paraméter elfogadható értékei: Tcp vagy Udp.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ef7a4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef7a4-141">-Confirm</span></span>
<span data-ttu-id="ef7a4-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7a4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7a4-143">-WhatIf</span></span>
<span data-ttu-id="ef7a4-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef7a4-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7a4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7a4-146">CommonParameters</span></span>
<span data-ttu-id="ef7a4-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7a4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7a4-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7a4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7a4-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef7a4-149">INPUTS</span></span>

### <span data-ttu-id="ef7a4-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef7a4-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ef7a4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="ef7a4-151">System.String</span></span>

### <span data-ttu-id="ef7a4-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ef7a4-152">System.Int32</span></span>

### <span data-ttu-id="ef7a4-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef7a4-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ef7a4-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef7a4-154">OUTPUTS</span></span>

### <span data-ttu-id="ef7a4-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef7a4-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ef7a4-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef7a4-156">NOTES</span></span>

## <span data-ttu-id="ef7a4-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef7a4-157">RELATED LINKS</span></span>

[<span data-ttu-id="ef7a4-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7a4-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ef7a4-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef7a4-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ef7a4-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7a4-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ef7a4-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7a4-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ef7a4-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7a4-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


