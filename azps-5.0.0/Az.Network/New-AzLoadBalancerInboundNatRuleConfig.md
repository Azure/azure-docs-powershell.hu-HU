---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186403"
---
# <span data-ttu-id="2afca-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2afca-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2afca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2afca-102">SYNOPSIS</span></span>
<span data-ttu-id="2afca-103">Bejövő hálózati címfordítási szabály konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="2afca-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="2afca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2afca-104">SYNTAX</span></span>

### <span data-ttu-id="2afca-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2afca-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afca-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2afca-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2afca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2afca-107">DESCRIPTION</span></span>
<span data-ttu-id="2afca-108">A **New-AzLoadBalancerInboundNatRuleConfig** parancsmag beérkező hálózati címfordítási (NAT) szabály-konfigurációt hoz létre az Azure terheléselosztó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="2afca-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2afca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2afca-109">EXAMPLES</span></span>

### <span data-ttu-id="2afca-110">1. példa: bejövő hálózati címfordítási szabály konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="2afca-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="2afca-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2afca-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="2afca-112">A második parancs létrehozza a FrontendIpConfig01 nevű előtér-IP-konfigurációt a $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2afca-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="2afca-113">A harmadik parancs a MyInboundNatRule nevű bejövő NAT-szabály konfigurációját a $frontend előtér objektumával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2afca-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="2afca-114">A TCP protokoll meg van adva, és az előtér-végpont a 3389, ugyanaz, mint a backend port ebben az esetben.</span><span class="sxs-lookup"><span data-stu-id="2afca-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="2afca-115">A *FrontendIpConfiguration* , a *Protocol* , a *FrontendPort* és a *BackendPort* paraméter mind szükséges a bejövő címfordítási szabályok konfigurációjának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="2afca-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="2afca-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2afca-116">PARAMETERS</span></span>

### <span data-ttu-id="2afca-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="2afca-117">-BackendPort</span></span>
<span data-ttu-id="2afca-118">A beállítás által kiválasztott forgalom backend-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2afca-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="2afca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afca-119">-DefaultProfile</span></span>
<span data-ttu-id="2afca-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2afca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2afca-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="2afca-121">-EnableFloatingIP</span></span>
<span data-ttu-id="2afca-122">Azt jelzi, hogy ez a parancsmag lehetővé teszi a szabályok konfigurációjának lebegő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="2afca-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="2afca-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2afca-123">-EnableTcpReset</span></span>
<span data-ttu-id="2afca-124">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="2afca-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="2afca-125">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="2afca-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2afca-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2afca-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2afca-127">A terheléselosztási szabályok konfigurációjával társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2afca-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2afca-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2afca-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="2afca-129">Az IP-címek konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2afca-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="2afca-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2afca-130">-FrontendPort</span></span>
<span data-ttu-id="2afca-131">A terheléselosztási szabályok konfigurációjának megfelelő előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2afca-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2afca-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2afca-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2afca-133">Azt adja meg, hogy hány percen belül maradjon a beszélgetések állapota a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="2afca-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="2afca-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2afca-134">-Name</span></span>
<span data-ttu-id="2afca-135">A parancsmag által létrehozott szabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2afca-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2afca-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2afca-136">-Protocol</span></span>
<span data-ttu-id="2afca-137">Egy protokollt ad meg.</span><span class="sxs-lookup"><span data-stu-id="2afca-137">Specifies a protocol.</span></span>
<span data-ttu-id="2afca-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2afca-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2afca-139">TCP</span><span class="sxs-lookup"><span data-stu-id="2afca-139">Tcp</span></span>
- <span data-ttu-id="2afca-140">UDP</span><span class="sxs-lookup"><span data-stu-id="2afca-140">Udp</span></span>

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

### <span data-ttu-id="2afca-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2afca-141">-Confirm</span></span>
<span data-ttu-id="2afca-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2afca-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2afca-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2afca-143">-WhatIf</span></span>
<span data-ttu-id="2afca-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2afca-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2afca-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2afca-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2afca-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afca-146">CommonParameters</span></span>
<span data-ttu-id="2afca-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2afca-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afca-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afca-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afca-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2afca-149">INPUTS</span></span>

### <span data-ttu-id="2afca-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2afca-150">System.String</span></span>

### <span data-ttu-id="2afca-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2afca-151">System.Int32</span></span>

### <span data-ttu-id="2afca-152">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2afca-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="2afca-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2afca-153">OUTPUTS</span></span>

### <span data-ttu-id="2afca-154">Microsoft. Azure. commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2afca-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="2afca-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2afca-155">NOTES</span></span>

## <span data-ttu-id="2afca-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2afca-156">RELATED LINKS</span></span>

[<span data-ttu-id="2afca-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2afca-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2afca-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2afca-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2afca-159">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2afca-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2afca-160">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2afca-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="2afca-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2afca-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2afca-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2afca-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


