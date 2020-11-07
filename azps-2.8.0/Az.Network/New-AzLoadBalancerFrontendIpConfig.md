---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: dc28df7630cbb2c9e239fe31f99ad3361e5c1f54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837198"
---
# <span data-ttu-id="11118-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11118-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="11118-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11118-102">SYNOPSIS</span></span>
<span data-ttu-id="11118-103">Előtér IP-konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="11118-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="11118-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11118-104">SYNTAX</span></span>

### <span data-ttu-id="11118-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11118-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11118-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="11118-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11118-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11118-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11118-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11118-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11118-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="11118-109">DESCRIPTION</span></span>
<span data-ttu-id="11118-110">A **New-AzLoadBalancerFrontendIpConfig** parancsmag az Azure-terheléselosztás előtér-IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="11118-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="11118-111">Példák</span><span class="sxs-lookup"><span data-stu-id="11118-111">EXAMPLES</span></span>

### <span data-ttu-id="11118-112">1. példa: az előtér IP-konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="11118-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="11118-113">Az első parancs létrehoz egy MyPublicIP nevű dinamikus nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="11118-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="11118-114">A második parancs a FrontendIpConfig01 nevű előtér IP-konfigurációját a $publicip nyilvános IP-címével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="11118-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="11118-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11118-115">PARAMETERS</span></span>

### <span data-ttu-id="11118-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11118-116">-DefaultProfile</span></span>
<span data-ttu-id="11118-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11118-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11118-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11118-118">-Name</span></span>
<span data-ttu-id="11118-119">A parancsmag által létrehozott előtér IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="11118-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11118-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="11118-120">-PrivateIpAddress</span></span>
<span data-ttu-id="11118-121">A terheléselosztó privát IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11118-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="11118-122">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="11118-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="11118-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="11118-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="11118-124">Az IP-konfiguráció privát IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="11118-124">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="11118-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11118-125">-PublicIpAddress</span></span>
<span data-ttu-id="11118-126">Azt a **PublicIpAddress** objektumot adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="11118-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="11118-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="11118-127">-PublicIpAddressId</span></span>
<span data-ttu-id="11118-128">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="11118-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="11118-129">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="11118-129">-Subnet</span></span>
<span data-ttu-id="11118-130">Annak az **alhálózati** objektumnak a meghatározása, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="11118-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="11118-131">– NetI</span><span class="sxs-lookup"><span data-stu-id="11118-131">-SubnetId</span></span>
<span data-ttu-id="11118-132">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="11118-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="11118-133">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="11118-133">-Zone</span></span>
<span data-ttu-id="11118-134">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="11118-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="11118-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11118-135">-Confirm</span></span>
<span data-ttu-id="11118-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11118-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11118-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11118-137">-WhatIf</span></span>
<span data-ttu-id="11118-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11118-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11118-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11118-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11118-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11118-140">CommonParameters</span></span>
<span data-ttu-id="11118-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11118-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11118-142">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11118-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11118-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11118-143">INPUTS</span></span>

### <span data-ttu-id="11118-144">System. String</span><span class="sxs-lookup"><span data-stu-id="11118-144">System.String</span></span>

### <span data-ttu-id="11118-145">System. string []</span><span class="sxs-lookup"><span data-stu-id="11118-145">System.String[]</span></span>

### <span data-ttu-id="11118-146">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="11118-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="11118-147">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11118-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="11118-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11118-148">OUTPUTS</span></span>

### <span data-ttu-id="11118-149">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11118-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="11118-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11118-150">NOTES</span></span>

## <span data-ttu-id="11118-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11118-151">RELATED LINKS</span></span>

[<span data-ttu-id="11118-152">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11118-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="11118-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11118-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="11118-154">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11118-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="11118-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11118-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="11118-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11118-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


