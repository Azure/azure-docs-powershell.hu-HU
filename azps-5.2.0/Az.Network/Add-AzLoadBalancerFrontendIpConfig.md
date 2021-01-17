---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361547"
---
# <span data-ttu-id="c7959-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7959-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="c7959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7959-102">SYNOPSIS</span></span>
<span data-ttu-id="c7959-103">Előlapi IP-konfigurációt ad a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c7959-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="c7959-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7959-104">SYNTAX</span></span>

### <span data-ttu-id="c7959-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7959-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7959-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="c7959-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7959-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7959-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7959-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7959-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7959-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c7959-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7959-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c7959-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7959-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7959-111">DESCRIPTION</span></span>
<span data-ttu-id="c7959-112">Az **Add-AzLoadBalancerFrontendIpConfig** parancsmag előtér-IP-konfigurációt ad az Azure terheléseloszlítóhoz.</span><span class="sxs-lookup"><span data-stu-id="c7959-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c7959-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7959-113">EXAMPLES</span></span>

### <span data-ttu-id="c7959-114">1. példa: Előlapi IP-konfiguráció hozzáadása dinamikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="c7959-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="c7959-115">Az első parancs leküldi a MyVnet nevű Azure virtuális hálózatot, és a folyamat segítségével átadja az eredményt a MySubnet nevű alhálózatnak a **Get-AzVirtualNetworkSubnetConfig** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c7959-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="c7959-116">A parancs ezután az eredményt a következő nevű változóban $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c7959-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="c7959-117">A második parancs leküldi a MyLB nevű terheléselegyenítőt, és átadja az eredményt az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely hozzáad egy előtér-IP-konfigurációt a terheléseloszlítóhoz egy dinamikus privát IP-címmel az $MySubnet nevű változóban tárolt alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="c7959-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="c7959-118">2. példa: Előlapi IP-konfiguráció hozzáadása statikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="c7959-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="c7959-119">Az első parancs leküldi a MyVnet nevű Azure virtuális hálózatot, és a folyamat segítségével átadja az eredményt a MySubnet nevű alhálózatnak a **Get-AzVirtualNetworkSubnetConfig** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c7959-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="c7959-120">A parancs ezután az eredményt a következő nevű változóban $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c7959-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="c7959-121">A második parancs leküldi a MyLB nevű terheléselegyenítőt, és átadja az eredményt az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely hozzáad egy előtér-IP-konfigurációt a terheléselegyenlőhez egy statikus privát IP-címmel az $Subnet nevű változóban tárolt alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="c7959-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="c7959-122">3. példa: Előlapi IP-konfiguráció beállítása nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="c7959-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="c7959-123">Az első parancs a MyPub nevű Azure nyilvános IP-címet kapja meg, és az eredményt a következő nevű változóban $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="c7959-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="c7959-124">A második parancs leküldi a MyLB nevű terheléselegyenítőt, és átadja az eredményt az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely egy előlapi IP-konfigurációt ad a terheléselegyenlőnek, és a $PublicIp nevű változóban tárolt nyilvános IP-címet tárol.</span><span class="sxs-lookup"><span data-stu-id="c7959-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="c7959-125">4. példa: Előlapi IP-konfiguráció beállítása nyilvános IP-előtaggal</span><span class="sxs-lookup"><span data-stu-id="c7959-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="c7959-126">Az első parancs az Azure nyilvános IP-előtagját (MyPubPrefix) kapja meg, és az eredményt a "MyPubPrefix" nevű változóban $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="c7959-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="c7959-127">A második parancs leküldi a MyLB nevű terheléselegyenítőt, és átadja az eredményt az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely hozzáad egy előtűnés IP-konfigurációt a terheléseloszlítóhoz a $PublicIpPrefix nevű változóban tárolt nyilvános IP-előtaggal.</span><span class="sxs-lookup"><span data-stu-id="c7959-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="c7959-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7959-128">PARAMETERS</span></span>

### <span data-ttu-id="c7959-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7959-129">-DefaultProfile</span></span>
<span data-ttu-id="c7959-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7959-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7959-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7959-131">-LoadBalancer</span></span>
<span data-ttu-id="c7959-132">Egy **LoadBalancer-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="c7959-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c7959-133">Ez a parancsmag hozzáad egy előlapi IP-konfigurációt a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c7959-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7959-134">-Name</span><span class="sxs-lookup"><span data-stu-id="c7959-134">-Name</span></span>
<span data-ttu-id="c7959-135">Az előlapi IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7959-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="c7959-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7959-136">-PrivateIpAddress</span></span>
<span data-ttu-id="c7959-137">Az előlapi IP-konfigurációhoz társítni szükséges személyes IP-cím.</span><span class="sxs-lookup"><span data-stu-id="c7959-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c7959-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="c7959-139">Az IP-konfiguráció privát IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="c7959-139">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7959-140">-PublicIpAddress</span></span>
<span data-ttu-id="c7959-141">Az előlapi IP-konfigurációhoz társítni szükséges nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="c7959-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c7959-142">-PublicIpAddressId</span></span>
<span data-ttu-id="c7959-143">Annak a nyilvános IP-címnek az azonosítója, amelyhez előlapi IP-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="c7959-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c7959-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="c7959-145">Az előlapi IP-konfigurációhoz társítni szükséges nyilvános IP-cím előtagjának objektuma.</span><span class="sxs-lookup"><span data-stu-id="c7959-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="c7959-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="c7959-147">Annak a nyilvános IP-cím előtag-objektumnak az azonosítója, amely előlapi IP-konfigurációval társítva van.</span><span class="sxs-lookup"><span data-stu-id="c7959-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-148">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="c7959-148">-Subnet</span></span>
<span data-ttu-id="c7959-149">Megadja azt az alhálózati objektumot, amelyben előtér-IP-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="c7959-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c7959-150">-SubnetId</span></span>
<span data-ttu-id="c7959-151">Annak az alhálózatnak az azonosítója, amelyhez előtér-IP-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="c7959-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="c7959-152">-Zone</span></span>
<span data-ttu-id="c7959-153">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="c7959-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7959-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7959-154">-Confirm</span></span>
<span data-ttu-id="c7959-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7959-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7959-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7959-156">-WhatIf</span></span>
<span data-ttu-id="c7959-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7959-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7959-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7959-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7959-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7959-159">CommonParameters</span></span>
<span data-ttu-id="c7959-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7959-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7959-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7959-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7959-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7959-162">INPUTS</span></span>

### <span data-ttu-id="c7959-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7959-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c7959-164">System.String</span><span class="sxs-lookup"><span data-stu-id="c7959-164">System.String</span></span>

### <span data-ttu-id="c7959-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c7959-165">System.String[]</span></span>

### <span data-ttu-id="c7959-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c7959-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="c7959-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7959-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c7959-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7959-168">OUTPUTS</span></span>

### <span data-ttu-id="c7959-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7959-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c7959-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7959-170">NOTES</span></span>

## <span data-ttu-id="c7959-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7959-171">RELATED LINKS</span></span>

[<span data-ttu-id="c7959-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7959-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c7959-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7959-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="c7959-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c7959-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c7959-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7959-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c7959-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7959-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c7959-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7959-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


