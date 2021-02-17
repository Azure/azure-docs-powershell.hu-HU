---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146882"
---
# <span data-ttu-id="bfbff-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfbff-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="bfbff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfbff-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbff-103">Előlapi IP-konfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="bfbff-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="bfbff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfbff-104">SYNTAX</span></span>

### <span data-ttu-id="bfbff-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfbff-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbff-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="bfbff-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbff-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfbff-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbff-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfbff-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbff-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bfbff-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbff-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bfbff-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfbff-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfbff-111">DESCRIPTION</span></span>
<span data-ttu-id="bfbff-112">A **New-AzLoadBalancerFrontendIpConfig** parancsmag előtér-IP-konfigurációt hoz létre egy Azure terheléselegyenítő számára.</span><span class="sxs-lookup"><span data-stu-id="bfbff-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="bfbff-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfbff-113">EXAMPLES</span></span>

### <span data-ttu-id="bfbff-114">1. példa: Előlapi IP-konfiguráció létrehozása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="bfbff-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="bfbff-115">Az első parancs létrehoz egy MyPublicIP nevű dinamikus nyilvános IP-címet a MyResourceGroup nevű erőforráscsoportban, majd tárolja azt a $publicip változóban.</span><span class="sxs-lookup"><span data-stu-id="bfbff-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="bfbff-116">A második parancs létrehoz egy FrontendIpConfig01 nevű előlapi IP-konfigurációt a nyilvános IP-cím használatával a $publicip.</span><span class="sxs-lookup"><span data-stu-id="bfbff-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="bfbff-117">2. példa: Előlapi IP-konfiguráció létrehozása terheléselosztáshoz ip-előtag használatával</span><span class="sxs-lookup"><span data-stu-id="bfbff-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="bfbff-118">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-előtagot (28 hosszú) a MyResourceGroup nevű erőforráscsoportban, majd tárolja azt a $publicipprefix változóban.</span><span class="sxs-lookup"><span data-stu-id="bfbff-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="bfbff-119">A második parancs létrehoz egy FrontendIpConfig01 nevű előlapi IP-konfigurációt a nyilvános IP-előtag használatával a $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="bfbff-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="bfbff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfbff-120">PARAMETERS</span></span>

### <span data-ttu-id="bfbff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbff-121">-DefaultProfile</span></span>
<span data-ttu-id="bfbff-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfbff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfbff-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bfbff-123">-Name</span></span>
<span data-ttu-id="bfbff-124">Ez a parancsmag által létrehozott előlapi IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfbff-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bfbff-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfbff-125">-PrivateIpAddress</span></span>
<span data-ttu-id="bfbff-126">A terheléselosztás magánjellegű IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfbff-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="bfbff-127">Ezt a paramétert csak akkor adja meg, ha az *Alhálózat paramétert* is megadja.</span><span class="sxs-lookup"><span data-stu-id="bfbff-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="bfbff-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bfbff-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="bfbff-129">Az IP-konfiguráció privát IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="bfbff-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfbff-130">-PublicIpAddress</span></span>
<span data-ttu-id="bfbff-131">Az előlapi IP-konfigurációhoz társítni szükséges **PublicIpAddress** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfbff-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bfbff-132">-PublicIpAddressId</span></span>
<span data-ttu-id="bfbff-133">Annak a **PublicIpAddress objektumnak** az azonosítója, amely előlapi IP-konfigurációval társítva van.</span><span class="sxs-lookup"><span data-stu-id="bfbff-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bfbff-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="bfbff-135">Az előlapi IP-konfigurációhoz társítni szükséges **PublicIpAddressPrefix** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfbff-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="bfbff-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="bfbff-137">Annak a **PublicIpAddressPrefix** objektumnak az azonosítója, amely előlapi IP-konfigurációval társítva van.</span><span class="sxs-lookup"><span data-stu-id="bfbff-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-138">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="bfbff-138">-Subnet</span></span>
<span data-ttu-id="bfbff-139">Azt az **alhálózati** objektumot adja meg, amelyben előtér-IP-konfigurációt kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bfbff-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bfbff-140">-SubnetId</span></span>
<span data-ttu-id="bfbff-141">Annak az alhálózatnak az azonosítója, amelyben előtér-IP-konfigurációt kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bfbff-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfbff-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="bfbff-142">-Zone</span></span>
<span data-ttu-id="bfbff-143">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="bfbff-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="bfbff-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfbff-144">-Confirm</span></span>
<span data-ttu-id="bfbff-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bfbff-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbff-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbff-146">-WhatIf</span></span>
<span data-ttu-id="bfbff-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bfbff-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfbff-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfbff-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbff-149">CommonParameters</span></span>
<span data-ttu-id="bfbff-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfbff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbff-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfbff-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbff-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfbff-152">INPUTS</span></span>

### <span data-ttu-id="bfbff-153">System.String</span><span class="sxs-lookup"><span data-stu-id="bfbff-153">System.String</span></span>

### <span data-ttu-id="bfbff-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bfbff-154">System.String[]</span></span>

### <span data-ttu-id="bfbff-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="bfbff-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="bfbff-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfbff-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bfbff-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfbff-157">OUTPUTS</span></span>

### <span data-ttu-id="bfbff-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfbff-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="bfbff-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfbff-159">NOTES</span></span>

## <span data-ttu-id="bfbff-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfbff-160">RELATED LINKS</span></span>

[<span data-ttu-id="bfbff-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfbff-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bfbff-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfbff-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bfbff-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfbff-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bfbff-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfbff-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bfbff-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfbff-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


