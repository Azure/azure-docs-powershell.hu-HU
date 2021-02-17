---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146923"
---
# <span data-ttu-id="efb27-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="efb27-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="efb27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb27-102">SYNOPSIS</span></span>
<span data-ttu-id="efb27-103">Terheléselosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="efb27-103">Creates a load balancer.</span></span>

## <span data-ttu-id="efb27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efb27-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efb27-105">DESCRIPTION</span></span>
<span data-ttu-id="efb27-106">A **New-AzLoadBalancer** parancsmag létrehoz egy Azure terheléselosztási törlőt.</span><span class="sxs-lookup"><span data-stu-id="efb27-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="efb27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efb27-107">EXAMPLES</span></span>

### <span data-ttu-id="efb27-108">1. példa: Terheléselosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="efb27-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="efb27-109">A terheléselosztás üzembe helyezéséhez először több objektumot kell létrehoznia, és az első hét parancs azt mutatja be, hogy miként hozhatja létre ezeket az objektumokat.</span><span class="sxs-lookup"><span data-stu-id="efb27-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="efb27-110">A nyolcadik parancs létrehoz egy MyLoadBalancer nevű terheléselosztást a MyResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="efb27-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="efb27-111">A kilencedik és az utolsó parancs megkapja az új terheléselosztást, hogy biztosítsa a sikeres létrehozást.</span><span class="sxs-lookup"><span data-stu-id="efb27-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="efb27-112">Ne feledje, hogy ez a példa csak azt mutatja be, hogy miként hozhat létre terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="efb27-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="efb27-113">A NIC-eket a Add-AzNetworkInterfaceIpConfig virtuális gépekhez való hozzárendeléshez a Add-AzNetworkInterfaceIpConfig kell konfigurálnia.</span><span class="sxs-lookup"><span data-stu-id="efb27-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="efb27-114">2. példa: Globális terheléselosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="efb27-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="efb27-115">A globális terheléselosztás telepítéséhez először több objektumot kell létrehoznia, és az első öt parancs azt mutatja be, hogy miként hozhatja létre ezeket az objektumokat.</span><span class="sxs-lookup"><span data-stu-id="efb27-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="efb27-116">A hatodik parancs létrehoz egy MyLoadBalancer nevű terheléselosztást a MyResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="efb27-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="efb27-117">A hetedik és az utolsó parancs megkapja az új terheléselosztást, hogy biztosítsa a sikeres létrejöttét.</span><span class="sxs-lookup"><span data-stu-id="efb27-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="efb27-118">Ne feledje, hogy ez a példa csak azt mutatja be, hogy miként hozhat létre globális terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="efb27-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="efb27-119">Azt is be kell állítania a New-AzLoadBalancerBackendAddressConfig parancsmaggal, hogy hozzárendelje a helyi terheléselegyenítő frontend ipconfig azonosítóit a háttércímkészlethez.</span><span class="sxs-lookup"><span data-stu-id="efb27-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="efb27-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efb27-120">PARAMETERS</span></span>

### <span data-ttu-id="efb27-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efb27-121">-AsJob</span></span>
<span data-ttu-id="efb27-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="efb27-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efb27-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb27-123">-BackendAddressPool</span></span>
<span data-ttu-id="efb27-124">Egy háttércímkészletet ad meg, amely a terheléskiegyenlítővel társítható.</span><span class="sxs-lookup"><span data-stu-id="efb27-124">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb27-125">-DefaultProfile</span></span>
<span data-ttu-id="efb27-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efb27-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efb27-127">-Force</span><span class="sxs-lookup"><span data-stu-id="efb27-127">-Force</span></span>
<span data-ttu-id="efb27-128">Azt jelzi, hogy ez a parancsmag akkor is hoz létre terheléselosztást, ha már létezik ilyen nevű terheléselosztási eszköz.</span><span class="sxs-lookup"><span data-stu-id="efb27-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="efb27-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="efb27-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="efb27-130">Megadja az előlapi IP-címek listáját, amelyek a terheléselosztáshoz társítva vannak.</span><span class="sxs-lookup"><span data-stu-id="efb27-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="efb27-131">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="efb27-132">-InboundNatRule</span></span>
<span data-ttu-id="efb27-133">Megadja a hálózati címfordítási (NAT) szabályok listáját, amelyek a terheléskiegyenlítóvel társítva vannak.</span><span class="sxs-lookup"><span data-stu-id="efb27-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="efb27-134">-LoadBalancingRule</span></span>
<span data-ttu-id="efb27-135">Megadja a terheléselosztási szabályok listáját, amelyek a terheléselosztási szabályokkal társítva vannak.</span><span class="sxs-lookup"><span data-stu-id="efb27-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-136">-Location</span><span class="sxs-lookup"><span data-stu-id="efb27-136">-Location</span></span>
<span data-ttu-id="efb27-137">Azt a régiót adja meg, amelyben terheléselosztást kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="efb27-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="efb27-138">-Name</span><span class="sxs-lookup"><span data-stu-id="efb27-138">-Name</span></span>
<span data-ttu-id="efb27-139">A létrehozott terheléselosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efb27-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="efb27-140">-KimenőSzabály</span><span class="sxs-lookup"><span data-stu-id="efb27-140">-OutboundRule</span></span>
<span data-ttu-id="efb27-141">A kimenő szabályok.</span><span class="sxs-lookup"><span data-stu-id="efb27-141">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-142">– Sivad</span><span class="sxs-lookup"><span data-stu-id="efb27-142">-Probe</span></span>
<span data-ttu-id="efb27-143">Megadja a terheléskiegyenléklővel társítva található törlőkedőket.</span><span class="sxs-lookup"><span data-stu-id="efb27-143">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb27-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb27-144">-ResourceGroupName</span></span>
<span data-ttu-id="efb27-145">Annak az erőforráscsoportnak a nevét adja meg, amelyben terheléselosztást kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="efb27-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="efb27-146">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="efb27-146">-Sku</span></span>
<span data-ttu-id="efb27-147">A terheléselosztási termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="efb27-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="efb27-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="efb27-148">-Tag</span></span>
<span data-ttu-id="efb27-149">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="efb27-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="efb27-150">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="efb27-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="efb27-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="efb27-151">-Tier</span></span>
<span data-ttu-id="efb27-152">A terheléselosztási termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="efb27-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="efb27-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efb27-153">-Confirm</span></span>
<span data-ttu-id="efb27-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efb27-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb27-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb27-155">-WhatIf</span></span>
<span data-ttu-id="efb27-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efb27-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb27-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efb27-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb27-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb27-158">CommonParameters</span></span>
<span data-ttu-id="efb27-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb27-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb27-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efb27-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb27-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efb27-161">INPUTS</span></span>

### <span data-ttu-id="efb27-162">System.String</span><span class="sxs-lookup"><span data-stu-id="efb27-162">System.String</span></span>

### <span data-ttu-id="efb27-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="efb27-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="efb27-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="efb27-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="efb27-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="efb27-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="efb27-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span><span class="sxs-lookup"><span data-stu-id="efb27-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="efb27-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="efb27-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="efb27-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="efb27-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="efb27-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="efb27-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="efb27-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="efb27-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="efb27-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efb27-171">OUTPUTS</span></span>

### <span data-ttu-id="efb27-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="efb27-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="efb27-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efb27-173">NOTES</span></span>

## <span data-ttu-id="efb27-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efb27-174">RELATED LINKS</span></span>

[<span data-ttu-id="efb27-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="efb27-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="efb27-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="efb27-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="efb27-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="efb27-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="efb27-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="efb27-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
