---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a6bec76345df188ca58e8b790637e35606de1f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001094"
---
# <span data-ttu-id="6bca4-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bca4-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="6bca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bca4-102">SYNOPSIS</span></span>
<span data-ttu-id="6bca4-103">Bejövő NAT-szabálykonfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="6bca4-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6bca4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6bca4-104">SYNTAX</span></span>

### <span data-ttu-id="6bca4-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bca4-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bca4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bca4-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bca4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6bca4-107">DESCRIPTION</span></span>
<span data-ttu-id="6bca4-108">A **New-AzLoadBalancerInboundNatRuleConfig** parancsmag létrehoz egy bejövő hálózati címfordítási (NAT) szabálykonfigurációt egy Azure-terheléselegyenlítóhoz.</span><span class="sxs-lookup"><span data-stu-id="6bca4-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6bca4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6bca4-109">EXAMPLES</span></span>

### <span data-ttu-id="6bca4-110">1. példa: Bejövő NAT-szabálykonfiguráció létrehozása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="6bca4-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="6bca4-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoportban, majd tárolja azt a $publicip változóban.</span><span class="sxs-lookup"><span data-stu-id="6bca4-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="6bca4-112">A második parancs létrehoz egy FrontendIpConfig01 nevű előlapi IP-konfigurációt az $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6bca4-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="6bca4-113">A harmadik parancs létrehoz egy MyInboundNatRule nevű bejövő NAT-szabályt a $frontend.</span><span class="sxs-lookup"><span data-stu-id="6bca4-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="6bca4-114">A TCP-protokoll meg van adva, az előlapi port pedig 3389, amely ebben az esetben megegyezik a háttérporttal.</span><span class="sxs-lookup"><span data-stu-id="6bca4-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="6bca4-115">A bejövő NAT-szabályok létrehozásához mind a *FrontendIpConfiguration, a* *Protocol,* a *FrontendPort* és a *BackendPort* paraméter szükséges.</span><span class="sxs-lookup"><span data-stu-id="6bca4-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="6bca4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bca4-116">PARAMETERS</span></span>

### <span data-ttu-id="6bca4-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6bca4-117">-BackendPort</span></span>
<span data-ttu-id="6bca4-118">Az ezzel a szabálykonfigurációval egyező forgalom háttér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bca4-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="6bca4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bca4-119">-DefaultProfile</span></span>
<span data-ttu-id="6bca4-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bca4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bca4-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6bca4-121">-EnableFloatingIP</span></span>
<span data-ttu-id="6bca4-122">Azt jelzi, hogy ez a parancsmag lebegő IP-címet tesz lehetővé egy szabálykonfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="6bca4-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6bca4-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="6bca4-123">-EnableTcpReset</span></span>
<span data-ttu-id="6bca4-124">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="6bca4-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6bca4-125">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="6bca4-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6bca4-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bca4-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6bca4-127">Megadja az előlapi IP-címek listáját, amelyek a terheléselosztási szabály konfigurációját társítják.</span><span class="sxs-lookup"><span data-stu-id="6bca4-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6bca4-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6bca4-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6bca4-129">Az előlapi IP-címek konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6bca4-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6bca4-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6bca4-130">-FrontendPort</span></span>
<span data-ttu-id="6bca4-131">Azt az előlapi portot adja meg, amelyet egy terheléselosztási szabály konfigurációja megfeleltet.</span><span class="sxs-lookup"><span data-stu-id="6bca4-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6bca4-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6bca4-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6bca4-133">Azt adja meg percben, hogy a rendszer mely időtartamra tartja fenn a beszélgetések állapotát a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="6bca4-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6bca4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="6bca4-134">-Name</span></span>
<span data-ttu-id="6bca4-135">A parancsmag által létrehozott szabálykonfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bca4-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6bca4-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6bca4-136">-Protocol</span></span>
<span data-ttu-id="6bca4-137">Protokollt ad meg.</span><span class="sxs-lookup"><span data-stu-id="6bca4-137">Specifies a protocol.</span></span>
<span data-ttu-id="6bca4-138">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="6bca4-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6bca4-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="6bca4-139">Tcp</span></span>
- <span data-ttu-id="6bca4-140">Udp</span><span class="sxs-lookup"><span data-stu-id="6bca4-140">Udp</span></span>

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

### <span data-ttu-id="6bca4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bca4-141">-Confirm</span></span>
<span data-ttu-id="6bca4-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6bca4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bca4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bca4-143">-WhatIf</span></span>
<span data-ttu-id="6bca4-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6bca4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bca4-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bca4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bca4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bca4-146">CommonParameters</span></span>
<span data-ttu-id="6bca4-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bca4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bca4-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bca4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bca4-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bca4-149">INPUTS</span></span>

### <span data-ttu-id="6bca4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6bca4-150">System.String</span></span>

### <span data-ttu-id="6bca4-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6bca4-151">System.Int32</span></span>

### <span data-ttu-id="6bca4-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bca4-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="6bca4-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bca4-153">OUTPUTS</span></span>

### <span data-ttu-id="6bca4-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="6bca4-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="6bca4-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6bca4-155">NOTES</span></span>

## <span data-ttu-id="6bca4-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bca4-156">RELATED LINKS</span></span>

[<span data-ttu-id="6bca4-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bca4-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6bca4-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bca4-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6bca4-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6bca4-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6bca4-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6bca4-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="6bca4-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bca4-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6bca4-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bca4-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


