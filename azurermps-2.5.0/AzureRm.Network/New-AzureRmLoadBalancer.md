---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 7abc575915eb65bf6c14994833bad64e6c7cd561
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849605"
---
# <span data-ttu-id="437f2-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="437f2-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="437f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="437f2-102">SYNOPSIS</span></span>
<span data-ttu-id="437f2-103">Terheléselosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="437f2-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="437f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="437f2-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="437f2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="437f2-105">DESCRIPTION</span></span>
<span data-ttu-id="437f2-106">A **New-AzureRmLoadBalancer** parancsmag az Azure terheléselosztó bővítményt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="437f2-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="437f2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="437f2-107">EXAMPLES</span></span>

### <span data-ttu-id="437f2-108">Példa 1: terheléselosztó létrehozása</span><span class="sxs-lookup"><span data-stu-id="437f2-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="437f2-109">A terheléselosztás központi telepítéséhez több objektum létrehozása szükséges, és az első hét parancs bemutatja, hogy miként hozhat létre ilyen objektumokat.</span><span class="sxs-lookup"><span data-stu-id="437f2-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="437f2-110">A nyolcadik parancs létrehoz egy MyLoadBalancer nevű terheléselosztást a MyResourceGroup nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="437f2-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="437f2-111">A kilencedik és az utolsó parancs az új terheléselosztást kapja annak érdekében, hogy sikeresen létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="437f2-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="437f2-112">Fontos tudni, hogy ez a példa csak azt szemlélteti, hogy miként hozhat létre terheléselosztót.</span><span class="sxs-lookup"><span data-stu-id="437f2-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="437f2-113">Az Add-AzureRmNetworkInterfaceIpConfig parancsmag használatával is konfigurálnia kell a hálózati adapterek különböző virtuális gépekhez való hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="437f2-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="437f2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="437f2-114">PARAMETERS</span></span>

### <span data-ttu-id="437f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="437f2-115">-AsJob</span></span>
<span data-ttu-id="437f2-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="437f2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="437f2-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="437f2-117">-BackendAddressPool</span></span>
<span data-ttu-id="437f2-118">A betöltőhöz társítani kívánt backend-címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="437f2-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="437f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="437f2-119">-DefaultProfile</span></span>
<span data-ttu-id="437f2-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="437f2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="437f2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="437f2-121">-Force</span></span>
<span data-ttu-id="437f2-122">Azt jelzi, hogy ez a parancsmag akkor is hoz létre terheléselosztást, ha már létezik ilyen nevű terheléselosztó.</span><span class="sxs-lookup"><span data-stu-id="437f2-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="437f2-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="437f2-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="437f2-124">A betöltőhöz társítani kívánt előtér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="437f2-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="437f2-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="437f2-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="437f2-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="437f2-126">-InboundNatRule</span></span>
<span data-ttu-id="437f2-127">A hálózati címfordításhoz kapcsolódó beérkező hálózati címfordítási szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="437f2-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="437f2-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="437f2-128">-LoadBalancingRule</span></span>
<span data-ttu-id="437f2-129">Itt adhatja meg a terheléselosztáshoz társítani kívánt terheléselosztási szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="437f2-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="437f2-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="437f2-130">-Location</span></span>
<span data-ttu-id="437f2-131">Azt a régiót adja meg, ahol a terheléselosztó létrehozható.</span><span class="sxs-lookup"><span data-stu-id="437f2-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="437f2-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="437f2-132">-Name</span></span>
<span data-ttu-id="437f2-133">Itt adhatja meg a létrehozott terheléselosztó nevét.</span><span class="sxs-lookup"><span data-stu-id="437f2-133">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="437f2-134">-Szonda</span><span class="sxs-lookup"><span data-stu-id="437f2-134">-Probe</span></span>
<span data-ttu-id="437f2-135">A terheléselosztáshoz társítani kívánt Szondák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="437f2-135">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="437f2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="437f2-136">-ResourceGroupName</span></span>
<span data-ttu-id="437f2-137">Annak az erőforrás-csoportnak a nevét adja meg, amelybe terheléselosztó hozható létre.</span><span class="sxs-lookup"><span data-stu-id="437f2-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="437f2-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="437f2-138">-Sku</span></span>
<span data-ttu-id="437f2-139">A terheléselosztó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="437f2-139">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="437f2-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="437f2-140">-Tag</span></span>
<span data-ttu-id="437f2-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="437f2-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="437f2-142">Példa:</span><span class="sxs-lookup"><span data-stu-id="437f2-142">For example:</span></span>

<span data-ttu-id="437f2-143">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="437f2-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="437f2-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="437f2-144">-Confirm</span></span>
<span data-ttu-id="437f2-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="437f2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="437f2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="437f2-146">-WhatIf</span></span>
<span data-ttu-id="437f2-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="437f2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="437f2-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="437f2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="437f2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437f2-149">CommonParameters</span></span>
<span data-ttu-id="437f2-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="437f2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437f2-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="437f2-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437f2-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="437f2-152">INPUTS</span></span>

## <span data-ttu-id="437f2-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="437f2-153">OUTPUTS</span></span>

### <span data-ttu-id="437f2-154">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="437f2-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="437f2-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="437f2-155">NOTES</span></span>

## <span data-ttu-id="437f2-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="437f2-156">RELATED LINKS</span></span>

[<span data-ttu-id="437f2-157">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="437f2-157">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="437f2-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="437f2-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="437f2-159">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="437f2-159">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="437f2-160">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="437f2-160">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
