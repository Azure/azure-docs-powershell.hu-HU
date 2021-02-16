---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146563"
---
# <span data-ttu-id="6efe4-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6efe4-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="6efe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6efe4-102">SYNOPSIS</span></span>
<span data-ttu-id="6efe4-103">Egy terheléselosztási eszköz előlapi IP-konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="6efe4-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="6efe4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6efe4-104">SYNTAX</span></span>

### <span data-ttu-id="6efe4-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6efe4-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe4-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="6efe4-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe4-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6efe4-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6efe4-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6efe4-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6efe4-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6efe4-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6efe4-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6efe4-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6efe4-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6efe4-111">DESCRIPTION</span></span>
<span data-ttu-id="6efe4-112">A **Set-AzLoadBalancerFrontendIpConfig** parancsmag egy terheléselegyenítő előlapi IP-konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="6efe4-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="6efe4-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6efe4-113">EXAMPLES</span></span>

### <span data-ttu-id="6efe4-114">1. példa: Terhelésegyenleg-kiegyensúlyozó előlapi IP-konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="6efe4-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="6efe4-115">Az első parancs megkapja az Alhálózat nevű virtuális alhálózatot, majd tárolja azt a $Subnet változóban.</span><span class="sxs-lookup"><span data-stu-id="6efe4-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6efe4-116">A második parancs lekérte a MyLoadBalancer nevű társított terheléselosztási törlőt, majd tárolja azt a $slb változóban.</span><span class="sxs-lookup"><span data-stu-id="6efe4-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="6efe4-117">A harmadik parancs a folyamat műveleti jelével adja át a terheléseloszlőt az $slb-nek az Add-AzLoadBalancerFrontendIpConfig bővítménynek, amely létrehozza a NewFrontend nevű előlapi IP-konfigurációt $slb.</span><span class="sxs-lookup"><span data-stu-id="6efe4-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="6efe4-118">A negyedik parancs átadja a $slb terheléselegyenítőt a **Set-AzLoadBalancerFrontendIpConfig** parancsnak, amely menti és frissíti az előlapi IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6efe4-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="6efe4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6efe4-119">PARAMETERS</span></span>

### <span data-ttu-id="6efe4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efe4-120">-DefaultProfile</span></span>
<span data-ttu-id="6efe4-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6efe4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6efe4-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6efe4-122">-LoadBalancer</span></span>
<span data-ttu-id="6efe4-123">Terheléselosztást ad meg.</span><span class="sxs-lookup"><span data-stu-id="6efe4-123">Specifies a load balancer.</span></span>
<span data-ttu-id="6efe4-124">Ez a parancsmag frissíti az előlapi konfigurációt a paraméter által megadott terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="6efe4-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6efe4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6efe4-125">-Name</span></span>
<span data-ttu-id="6efe4-126">A beállítani szükséges előlapi IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6efe4-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="6efe4-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6efe4-127">-PrivateIpAddress</span></span>
<span data-ttu-id="6efe4-128">Az előlapi IP-konfigurációhoz társított terheléselosztási kiszolgáló személyes IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6efe4-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="6efe4-129">Ezt a paramétert csak akkor adja meg, ha az *Alhálózat paramétert* is megadja.</span><span class="sxs-lookup"><span data-stu-id="6efe4-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="6efe4-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6efe4-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="6efe4-131">Az IP-konfiguráció privát IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="6efe4-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="6efe4-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6efe4-132">-PublicIpAddress</span></span>
<span data-ttu-id="6efe4-133">Az előlapi IP-konfigurációval társított **PublicIpAddress** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6efe4-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="6efe4-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6efe4-134">-PublicIpAddressId</span></span>
<span data-ttu-id="6efe4-135">Annak a **PublicIpAddress** objektumnak az azonosítója, amely a parancsmag által megadott előlapi IP-konfigurációhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="6efe4-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="6efe4-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6efe4-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="6efe4-137">A **PublicIpAddressPrefix** objektumot adja meg, amely előlapi IP-konfigurációval társítva van.</span><span class="sxs-lookup"><span data-stu-id="6efe4-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6efe4-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="6efe4-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="6efe4-139">Annak a **PublicIpAddressPrefix** objektumnak az azonosítója, amely előlapi IP-konfigurációval társítva van.</span><span class="sxs-lookup"><span data-stu-id="6efe4-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6efe4-140">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="6efe4-140">-Subnet</span></span>
<span data-ttu-id="6efe4-141">Megadja azt az **alhálózati** objektumot, amely a parancsmag által megadott előtér-IP-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6efe4-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="6efe4-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6efe4-142">-SubnetId</span></span>
<span data-ttu-id="6efe4-143">Annak az alhálózatnak az azonosítója, amely a parancsmag által megadott előtér-IP-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6efe4-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="6efe4-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="6efe4-144">-Zone</span></span>
<span data-ttu-id="6efe4-145">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="6efe4-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="6efe4-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6efe4-146">-Confirm</span></span>
<span data-ttu-id="6efe4-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6efe4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6efe4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6efe4-148">-WhatIf</span></span>
<span data-ttu-id="6efe4-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6efe4-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6efe4-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6efe4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6efe4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efe4-151">CommonParameters</span></span>
<span data-ttu-id="6efe4-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efe4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efe4-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6efe4-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efe4-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6efe4-154">INPUTS</span></span>

### <span data-ttu-id="6efe4-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6efe4-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6efe4-156">System.String</span><span class="sxs-lookup"><span data-stu-id="6efe4-156">System.String</span></span>

### <span data-ttu-id="6efe4-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6efe4-157">System.String[]</span></span>

### <span data-ttu-id="6efe4-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6efe4-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="6efe4-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6efe4-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="6efe4-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6efe4-160">OUTPUTS</span></span>

### <span data-ttu-id="6efe4-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6efe4-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6efe4-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6efe4-162">NOTES</span></span>

## <span data-ttu-id="6efe4-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6efe4-163">RELATED LINKS</span></span>

[<span data-ttu-id="6efe4-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6efe4-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6efe4-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6efe4-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6efe4-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6efe4-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6efe4-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6efe4-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="6efe4-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6efe4-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6efe4-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6efe4-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


