---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: db7d531b83dabe3bb5fc9dc79d86c3153d1553a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680639"
---
# <span data-ttu-id="38c2f-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38c2f-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="38c2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="38c2f-103">Terheléselosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="38c2f-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38c2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38c2f-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-OutboundRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c2f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="38c2f-106">A **New-AzureRmLoadBalancer** parancsmag az Azure terheléselosztó bővítményt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="38c2f-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="38c2f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="38c2f-108">Példa 1: terheléselosztó létrehozása</span><span class="sxs-lookup"><span data-stu-id="38c2f-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="38c2f-109">A terheléselosztás központi telepítéséhez több objektum létrehozása szükséges, és az első hét parancs bemutatja, hogy miként hozhat létre ilyen objektumokat.</span><span class="sxs-lookup"><span data-stu-id="38c2f-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="38c2f-110">A nyolcadik parancs létrehoz egy MyLoadBalancer nevű terheléselosztást a MyResourceGroup nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="38c2f-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="38c2f-111">A kilencedik és az utolsó parancs az új terheléselosztást kapja annak érdekében, hogy sikeresen létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="38c2f-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="38c2f-112">Fontos tudni, hogy ez a példa csak azt szemlélteti, hogy miként hozhat létre terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="38c2f-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="38c2f-113">Az Add-AzureRmNetworkInterfaceIpConfig parancsmag használatával is konfigurálnia kell a hálózati adapterek különböző virtuális gépekhez való hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="38c2f-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="38c2f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38c2f-114">PARAMETERS</span></span>

### <span data-ttu-id="38c2f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38c2f-115">-AsJob</span></span>
<span data-ttu-id="38c2f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="38c2f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c2f-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="38c2f-117">-BackendAddressPool</span></span>
<span data-ttu-id="38c2f-118">A betöltőhöz társítani kívánt backend-címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="38c2f-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c2f-119">-DefaultProfile</span></span>
<span data-ttu-id="38c2f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38c2f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38c2f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="38c2f-121">-Force</span></span>
<span data-ttu-id="38c2f-122">Azt jelzi, hogy ez a parancsmag akkor is hoz létre terheléselosztást, ha már létezik ilyen nevű terheléselosztó.</span><span class="sxs-lookup"><span data-stu-id="38c2f-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="38c2f-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="38c2f-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="38c2f-124">A betöltőhöz társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="38c2f-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="38c2f-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="38c2f-126">-InboundNatRule</span></span>
<span data-ttu-id="38c2f-127">A hálózati címfordításhoz kapcsolódó beérkező hálózati címfordítási szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="38c2f-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="38c2f-128">-LoadBalancingRule</span></span>
<span data-ttu-id="38c2f-129">Itt adhatja meg a terheléselosztáshoz társítani kívánt terheléselosztási szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="38c2f-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="38c2f-130">-Location</span></span>
<span data-ttu-id="38c2f-131">Azt a régiót adja meg, ahol a terheléselosztó létrehozható.</span><span class="sxs-lookup"><span data-stu-id="38c2f-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38c2f-132">-Name</span></span>
<span data-ttu-id="38c2f-133">Itt adhatja meg a létrehozott terheléselosztó nevét.</span><span class="sxs-lookup"><span data-stu-id="38c2f-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="38c2f-134">-OutboundRule</span></span>
<span data-ttu-id="38c2f-135">A kimenő szabályok.</span><span class="sxs-lookup"><span data-stu-id="38c2f-135">The outbound rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-136">-Szonda</span><span class="sxs-lookup"><span data-stu-id="38c2f-136">-Probe</span></span>
<span data-ttu-id="38c2f-137">A terheléselosztáshoz társítani kívánt Szondák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="38c2f-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c2f-138">-ResourceGroupName</span></span>
<span data-ttu-id="38c2f-139">Annak az erőforrás-csoportnak a nevét adja meg, amelybe terheléselosztó hozható létre.</span><span class="sxs-lookup"><span data-stu-id="38c2f-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="38c2f-140">-Sku</span></span>
<span data-ttu-id="38c2f-141">A terheléselosztó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="38c2f-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="38c2f-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="38c2f-142">-Tag</span></span>
<span data-ttu-id="38c2f-143">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="38c2f-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="38c2f-144">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="38c2f-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38c2f-145">-Confirm</span></span>
<span data-ttu-id="38c2f-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38c2f-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c2f-147">-WhatIf</span></span>
<span data-ttu-id="38c2f-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38c2f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c2f-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38c2f-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c2f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c2f-150">CommonParameters</span></span>
<span data-ttu-id="38c2f-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38c2f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c2f-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c2f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c2f-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38c2f-153">INPUTS</span></span>

### <span data-ttu-id="38c2f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="38c2f-154">System.String</span></span>

### <span data-ttu-id="38c2f-155">System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38c2f-155">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="38c2f-156">System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSBackendAddressPool, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38c2f-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="38c2f-157">System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSProbe, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38c2f-157">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="38c2f-158">System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSInboundNatRule, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38c2f-158">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="38c2f-159">System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSLoadBalancingRule, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38c2f-159">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="38c2f-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="38c2f-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="38c2f-161">System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSInboundNatPool, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38c2f-161">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="38c2f-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38c2f-162">OUTPUTS</span></span>

### <span data-ttu-id="38c2f-163">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38c2f-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="38c2f-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38c2f-164">NOTES</span></span>

## <span data-ttu-id="38c2f-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38c2f-165">RELATED LINKS</span></span>

[<span data-ttu-id="38c2f-166">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="38c2f-166">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="38c2f-167">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38c2f-167">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="38c2f-168">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38c2f-168">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="38c2f-169">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38c2f-169">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
