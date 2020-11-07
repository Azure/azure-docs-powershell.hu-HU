---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0299494ca775df60c94151f36efe554d0b876d22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670323"
---
# <span data-ttu-id="5b7a9-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b7a9-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5b7a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7a9-103">Előtér IP-konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="5b7a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b7a9-104">SYNTAX</span></span>

### <span data-ttu-id="5b7a9-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b7a9-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7a9-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5b7a9-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7a9-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b7a9-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7a9-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b7a9-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b7a9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b7a9-109">DESCRIPTION</span></span>
<span data-ttu-id="5b7a9-110">A **New-AzLoadBalancerFrontendIpConfig** parancsmag az Azure-terheléselosztás előtér-IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5b7a9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5b7a9-111">EXAMPLES</span></span>

### <span data-ttu-id="5b7a9-112">1. példa: az előtér IP-konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="5b7a9-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="5b7a9-113">Az első parancs létrehoz egy MyPublicIP nevű dinamikus nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="5b7a9-114">A második parancs a FrontendIpConfig01 nevű előtér IP-konfigurációját a $publicip nyilvános IP-címével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="5b7a9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b7a9-115">PARAMETERS</span></span>

### <span data-ttu-id="5b7a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7a9-116">-DefaultProfile</span></span>
<span data-ttu-id="5b7a9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b7a9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b7a9-118">-Name</span></span>
<span data-ttu-id="5b7a9-119">A parancsmag által létrehozott előtér IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5b7a9-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b7a9-120">-PrivateIpAddress</span></span>
<span data-ttu-id="5b7a9-121">A terheléselosztó privát IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="5b7a9-122">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="5b7a9-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b7a9-123">-PublicIpAddress</span></span>
<span data-ttu-id="5b7a9-124">Azt a **PublicIpAddress** objektumot adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5b7a9-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5b7a9-125">-PublicIpAddressId</span></span>
<span data-ttu-id="5b7a9-126">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5b7a9-127">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5b7a9-127">-Subnet</span></span>
<span data-ttu-id="5b7a9-128">Annak az **alhálózati** objektumnak a meghatározása, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5b7a9-129">– NetI</span><span class="sxs-lookup"><span data-stu-id="5b7a9-129">-SubnetId</span></span>
<span data-ttu-id="5b7a9-130">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5b7a9-131">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="5b7a9-131">-Zone</span></span>
<span data-ttu-id="5b7a9-132">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5b7a9-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b7a9-133">-Confirm</span></span>
<span data-ttu-id="5b7a9-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b7a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7a9-135">-WhatIf</span></span>
<span data-ttu-id="5b7a9-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b7a9-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b7a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b7a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7a9-138">CommonParameters</span></span>
<span data-ttu-id="5b7a9-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b7a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7a9-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b7a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7a9-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7a9-141">INPUTS</span></span>

### <span data-ttu-id="5b7a9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5b7a9-142">System.String</span></span>

### <span data-ttu-id="5b7a9-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="5b7a9-143">System.String[]</span></span>

### <span data-ttu-id="5b7a9-144">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5b7a9-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="5b7a9-145">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b7a9-145">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5b7a9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7a9-146">OUTPUTS</span></span>

### <span data-ttu-id="5b7a9-147">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b7a9-147">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="5b7a9-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b7a9-148">NOTES</span></span>

## <span data-ttu-id="5b7a9-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b7a9-149">RELATED LINKS</span></span>

[<span data-ttu-id="5b7a9-150">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b7a9-150">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5b7a9-151">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b7a9-151">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5b7a9-152">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b7a9-152">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="5b7a9-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b7a9-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5b7a9-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b7a9-154">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


