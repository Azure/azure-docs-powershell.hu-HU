---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bd8a5ef28d9ccc168df86d542156f709add87f52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837021"
---
# <span data-ttu-id="5f07e-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f07e-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5f07e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f07e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f07e-103">Az előtér IP-konfigurációjának frissítése a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="5f07e-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="5f07e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f07e-104">SYNTAX</span></span>

### <span data-ttu-id="5f07e-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f07e-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f07e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5f07e-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f07e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5f07e-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f07e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5f07e-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f07e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f07e-109">DESCRIPTION</span></span>
<span data-ttu-id="5f07e-110">A **set-AzLoadBalancerFrontendIpConfig** parancsmag az előtér IP-konfigurációját frissíti a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="5f07e-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="5f07e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5f07e-111">EXAMPLES</span></span>

### <span data-ttu-id="5f07e-112">Példa 1: a terheléselosztó előtér IP-konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="5f07e-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="5f07e-113">Az első parancs az alhálózat nevű virtuális alhálózatot kapja, majd a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5f07e-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="5f07e-114">A második parancs megkapja a MyLoadBalancer nevű társított terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5f07e-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="5f07e-115">A harmadik parancs a pipeline operátor segítségével átadja a terheléselosztást $slb a AzLoadBalancerFrontendIpConfig-hoz, amely egy, az $slbhoz NewFrontend nevű előtér IP-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5f07e-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="5f07e-116">A negyedik parancs átadja a terheléselosztást $slb a **set-AzLoadBalancerFrontendIpConfig** , amely az előtér IP-konfigurációját menti és frissíti.</span><span class="sxs-lookup"><span data-stu-id="5f07e-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="5f07e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f07e-117">PARAMETERS</span></span>

### <span data-ttu-id="5f07e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f07e-118">-DefaultProfile</span></span>
<span data-ttu-id="5f07e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f07e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f07e-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f07e-120">-LoadBalancer</span></span>
<span data-ttu-id="5f07e-121">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f07e-121">Specifies a load balancer.</span></span>
<span data-ttu-id="5f07e-122">Ez a parancsmag frissíti a paraméter által megadott terheléselosztó előtér-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5f07e-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f07e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f07e-123">-Name</span></span>
<span data-ttu-id="5f07e-124">A beállítani kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f07e-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="5f07e-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5f07e-125">-PrivateIpAddress</span></span>
<span data-ttu-id="5f07e-126">Annak a terheléselosztásnak a magánjellegű IP-címét adja meg, amely az előtér IP-konfigurációjáról van társítva.</span><span class="sxs-lookup"><span data-stu-id="5f07e-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="5f07e-127">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="5f07e-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="5f07e-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5f07e-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="5f07e-129">Az IP-konfiguráció privát IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="5f07e-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="5f07e-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5f07e-130">-PublicIpAddress</span></span>
<span data-ttu-id="5f07e-131">Megadja az **PublicIpAddress** -objektumot, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="5f07e-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="5f07e-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5f07e-132">-PublicIpAddressId</span></span>
<span data-ttu-id="5f07e-133">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amely a parancsmag által beállított előtér-IP-konfigurációhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="5f07e-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="5f07e-134">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5f07e-134">-Subnet</span></span>
<span data-ttu-id="5f07e-135">Azt az **alhálózati** objektumot adja meg, amely tartalmazza a parancsmag által beállított előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5f07e-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="5f07e-136">– NetI</span><span class="sxs-lookup"><span data-stu-id="5f07e-136">-SubnetId</span></span>
<span data-ttu-id="5f07e-137">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amely tartalmazza a parancsmag által beállított előtér-IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="5f07e-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="5f07e-138">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="5f07e-138">-Zone</span></span>
<span data-ttu-id="5f07e-139">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="5f07e-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5f07e-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f07e-140">-Confirm</span></span>
<span data-ttu-id="5f07e-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f07e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f07e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f07e-142">-WhatIf</span></span>
<span data-ttu-id="5f07e-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f07e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f07e-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f07e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f07e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f07e-145">CommonParameters</span></span>
<span data-ttu-id="5f07e-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f07e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f07e-147">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5f07e-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f07e-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f07e-148">INPUTS</span></span>

### <span data-ttu-id="5f07e-149">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f07e-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5f07e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5f07e-150">System.String</span></span>

### <span data-ttu-id="5f07e-151">System. string []</span><span class="sxs-lookup"><span data-stu-id="5f07e-151">System.String[]</span></span>

### <span data-ttu-id="5f07e-152">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5f07e-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="5f07e-153">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5f07e-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5f07e-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f07e-154">OUTPUTS</span></span>

### <span data-ttu-id="5f07e-155">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f07e-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5f07e-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f07e-156">NOTES</span></span>

## <span data-ttu-id="5f07e-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f07e-157">RELATED LINKS</span></span>

[<span data-ttu-id="5f07e-158">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f07e-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5f07e-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f07e-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5f07e-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f07e-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5f07e-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f07e-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5f07e-162">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f07e-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5f07e-163">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f07e-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


