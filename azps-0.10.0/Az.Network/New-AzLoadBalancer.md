---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: fac34080ed9b96c30c9003cef57f73f416711ac5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841358"
---
# <span data-ttu-id="6a2ba-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6a2ba-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="6a2ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2ba-103">Terheléselosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-103">Creates a load balancer.</span></span>

## <span data-ttu-id="6a2ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a2ba-104">SYNTAX</span></span>

```
New-AzLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a2ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a2ba-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2ba-106">A **New-AzLoadBalancer** parancsmag az Azure terheléselosztó bővítményt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="6a2ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a2ba-107">EXAMPLES</span></span>

### <span data-ttu-id="6a2ba-108">Példa 1: terheléselosztó létrehozása</span><span class="sxs-lookup"><span data-stu-id="6a2ba-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="6a2ba-109">A terheléselosztás központi telepítéséhez több objektum létrehozása szükséges, és az első hét parancs bemutatja, hogy miként hozhat létre ilyen objektumokat.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="6a2ba-110">A nyolcadik parancs létrehoz egy MyLoadBalancer nevű terheléselosztást a MyResourceGroup nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="6a2ba-111">A kilencedik és az utolsó parancs az új terheléselosztást kapja annak érdekében, hogy sikeresen létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="6a2ba-112">Fontos tudni, hogy ez a példa csak azt szemlélteti, hogy miként hozhat létre terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="6a2ba-113">Az Add-AzNetworkInterfaceIpConfig parancsmag használatával is konfigurálnia kell a hálózati adapterek különböző virtuális gépekhez való hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="6a2ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a2ba-114">PARAMETERS</span></span>

### <span data-ttu-id="6a2ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a2ba-115">-AsJob</span></span>
<span data-ttu-id="6a2ba-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6a2ba-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a2ba-117">-BackendAddressPool</span></span>
<span data-ttu-id="6a2ba-118">A betöltőhöz társítani kívánt backend-címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="6a2ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2ba-119">-DefaultProfile</span></span>
<span data-ttu-id="6a2ba-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6a2ba-121">-Force</span></span>
<span data-ttu-id="6a2ba-122">Azt jelzi, hogy ez a parancsmag akkor is hoz létre terheléselosztást, ha már létezik ilyen nevű terheléselosztó.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a2ba-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6a2ba-124">A betöltőhöz társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="6a2ba-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="6a2ba-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="6a2ba-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="6a2ba-126">-InboundNatRule</span></span>
<span data-ttu-id="6a2ba-127">A hálózati címfordításhoz kapcsolódó beérkező hálózati címfordítási szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="6a2ba-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="6a2ba-128">-LoadBalancingRule</span></span>
<span data-ttu-id="6a2ba-129">Itt adhatja meg a terheléselosztáshoz társítani kívánt terheléselosztási szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="6a2ba-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="6a2ba-130">-Location</span></span>
<span data-ttu-id="6a2ba-131">Azt a régiót adja meg, ahol a terheléselosztó létrehozható.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a2ba-132">-Name</span></span>
<span data-ttu-id="6a2ba-133">Itt adhatja meg a létrehozott terheléselosztó nevét.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-134">-Szonda</span><span class="sxs-lookup"><span data-stu-id="6a2ba-134">-Probe</span></span>
<span data-ttu-id="6a2ba-135">A terheléselosztáshoz társítani kívánt Szondák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-135">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="6a2ba-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a2ba-136">-ResourceGroupName</span></span>
<span data-ttu-id="6a2ba-137">Annak az erőforrás-csoportnak a nevét adja meg, amelybe terheléselosztó hozható létre.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="6a2ba-138">-Sku</span></span>
<span data-ttu-id="6a2ba-139">A terheléselosztó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="6a2ba-140">-Tag</span></span>
<span data-ttu-id="6a2ba-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a2ba-142">Példa:</span><span class="sxs-lookup"><span data-stu-id="6a2ba-142">For example:</span></span>

<span data-ttu-id="6a2ba-143">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="6a2ba-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a2ba-144">-Confirm</span></span>
<span data-ttu-id="6a2ba-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2ba-146">-WhatIf</span></span>
<span data-ttu-id="6a2ba-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a2ba-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a2ba-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2ba-149">CommonParameters</span></span>
<span data-ttu-id="6a2ba-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a2ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2ba-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2ba-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2ba-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a2ba-152">INPUTS</span></span>

## <span data-ttu-id="6a2ba-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a2ba-153">OUTPUTS</span></span>

### <span data-ttu-id="6a2ba-154">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6a2ba-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6a2ba-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a2ba-155">NOTES</span></span>

## <span data-ttu-id="6a2ba-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a2ba-156">RELATED LINKS</span></span>

[<span data-ttu-id="6a2ba-157">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6a2ba-157">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6a2ba-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6a2ba-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6a2ba-159">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6a2ba-159">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="6a2ba-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6a2ba-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
