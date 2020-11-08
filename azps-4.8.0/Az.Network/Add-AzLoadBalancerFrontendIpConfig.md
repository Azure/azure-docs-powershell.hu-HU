---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184896"
---
# <span data-ttu-id="f4e27-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e27-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f4e27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4e27-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e27-103">Az előtér IP-konfigurációját hozzáadja a terheléselosztó beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="f4e27-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="f4e27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4e27-104">SYNTAX</span></span>

### <span data-ttu-id="f4e27-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4e27-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e27-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f4e27-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e27-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4e27-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4e27-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4e27-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4e27-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4e27-109">DESCRIPTION</span></span>
<span data-ttu-id="f4e27-110">Az **Add-AzLoadBalancerFrontendIpConfig** parancsmag egy előtér-IP-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f4e27-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f4e27-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f4e27-111">EXAMPLES</span></span>

### <span data-ttu-id="f4e27-112">Példa: az előtér IP-konfigurációjának hozzáadása dinamikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="f4e27-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="f4e27-113">Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="f4e27-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f4e27-114">A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4e27-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f4e27-115">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, a $MySubnet nevű változóban tárolt dinamikus magánhálózati IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="f4e27-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="f4e27-116">Példa 2 az előtér IP-konfigurációjának hozzáadása statikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="f4e27-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="f4e27-117">Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="f4e27-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f4e27-118">A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4e27-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f4e27-119">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, az $subnet nevű változóban tárolt statikus magánhálózati IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="f4e27-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="f4e27-120">Példa 3 előtér IP-konfigurációjának hozzáadása nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="f4e27-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="f4e27-121">Az első parancs a MyPub nevű Azure nyilvános IP-címet kapja, és az eredményt az $PublicIp nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4e27-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="f4e27-122">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz az $PublicIp nevű változóban tárolt nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="f4e27-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="f4e27-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4e27-123">PARAMETERS</span></span>

### <span data-ttu-id="f4e27-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e27-124">-DefaultProfile</span></span>
<span data-ttu-id="f4e27-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4e27-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e27-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4e27-126">-LoadBalancer</span></span>
<span data-ttu-id="f4e27-127">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f4e27-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f4e27-128">Ez a parancsmag az előtér IP-konfigurációját hozzáadja a paraméter által megadott terheléselosztó típushoz.</span><span class="sxs-lookup"><span data-stu-id="f4e27-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e27-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4e27-129">-Name</span></span>
<span data-ttu-id="f4e27-130">A hozzáadni kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4e27-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="f4e27-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4e27-131">-PrivateIpAddress</span></span>
<span data-ttu-id="f4e27-132">Annak a magánhálózati IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="f4e27-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f4e27-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f4e27-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f4e27-134">Az IP-konfiguráció privát IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="f4e27-134">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="f4e27-135">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4e27-135">-PublicIpAddress</span></span>
<span data-ttu-id="f4e27-136">Annak a nyilvános IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="f4e27-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f4e27-137">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f4e27-137">-PublicIpAddressId</span></span>
<span data-ttu-id="f4e27-138">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f4e27-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f4e27-139">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="f4e27-139">-Subnet</span></span>
<span data-ttu-id="f4e27-140">Annak az alhálózati objektumnak a meghatározása, amelyben az előtér-IP-konfigurációt fel szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="f4e27-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f4e27-141">– NetI</span><span class="sxs-lookup"><span data-stu-id="f4e27-141">-SubnetId</span></span>
<span data-ttu-id="f4e27-142">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f4e27-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f4e27-143">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="f4e27-143">-Zone</span></span>
<span data-ttu-id="f4e27-144">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="f4e27-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f4e27-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4e27-145">-Confirm</span></span>
<span data-ttu-id="f4e27-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4e27-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e27-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e27-147">-WhatIf</span></span>
<span data-ttu-id="f4e27-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4e27-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4e27-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4e27-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e27-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e27-150">CommonParameters</span></span>
<span data-ttu-id="f4e27-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4e27-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e27-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4e27-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e27-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e27-153">INPUTS</span></span>

### <span data-ttu-id="f4e27-154">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4e27-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f4e27-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e27-155">System.String</span></span>

### <span data-ttu-id="f4e27-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="f4e27-156">System.String[]</span></span>

### <span data-ttu-id="f4e27-157">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f4e27-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f4e27-158">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4e27-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f4e27-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e27-159">OUTPUTS</span></span>

### <span data-ttu-id="f4e27-160">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4e27-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f4e27-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4e27-161">NOTES</span></span>

## <span data-ttu-id="f4e27-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4e27-162">RELATED LINKS</span></span>

[<span data-ttu-id="f4e27-163">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e27-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f4e27-164">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4e27-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f4e27-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f4e27-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f4e27-166">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e27-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f4e27-167">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e27-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f4e27-168">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e27-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


