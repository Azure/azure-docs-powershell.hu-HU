---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 77dbd80f03cb26adbb68e320d761200cd9ee7bc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495911"
---
# <span data-ttu-id="cd2dc-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd2dc-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="cd2dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2dc-103">Előtér IP-konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd2dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd2dc-104">SYNTAX</span></span>

### <span data-ttu-id="cd2dc-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd2dc-105">SetByResourceSubnet (Default)</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd2dc-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="cd2dc-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd2dc-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd2dc-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd2dc-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd2dc-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2dc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd2dc-109">DESCRIPTION</span></span>
<span data-ttu-id="cd2dc-110">A **New-AzureRmLoadBalancerFrontendIpConfig** parancsmag az Azure-terheléselosztás előtér-IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="cd2dc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cd2dc-111">EXAMPLES</span></span>

### <span data-ttu-id="cd2dc-112">1. példa: az előtér IP-konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="cd2dc-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="cd2dc-113">Az első parancs létrehoz egy MyPublicIP nevű dinamikus nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="cd2dc-114">A második parancs a FrontendIpConfig01 nevű előtér IP-konfigurációját a $publicip nyilvános IP-címével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="cd2dc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd2dc-115">PARAMETERS</span></span>

### <span data-ttu-id="cd2dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2dc-116">-DefaultProfile</span></span>
<span data-ttu-id="cd2dc-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2dc-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd2dc-118">-Name</span></span>
<span data-ttu-id="cd2dc-119">A parancsmag által létrehozott előtér IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cd2dc-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd2dc-120">-PrivateIpAddress</span></span>
<span data-ttu-id="cd2dc-121">A terheléselosztó privát IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="cd2dc-122">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="cd2dc-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd2dc-123">-PublicIpAddress</span></span>
<span data-ttu-id="cd2dc-124">Azt a **PublicIpAddress** objektumot adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="cd2dc-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="cd2dc-125">-PublicIpAddressId</span></span>
<span data-ttu-id="cd2dc-126">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="cd2dc-127">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="cd2dc-127">-Subnet</span></span>
<span data-ttu-id="cd2dc-128">Annak az **alhálózati** objektumnak a meghatározása, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="cd2dc-129">– NetI</span><span class="sxs-lookup"><span data-stu-id="cd2dc-129">-SubnetId</span></span>
<span data-ttu-id="cd2dc-130">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="cd2dc-131">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="cd2dc-131">-Zone</span></span>
<span data-ttu-id="cd2dc-132">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2dc-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd2dc-133">-Confirm</span></span>
<span data-ttu-id="cd2dc-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2dc-135">-WhatIf</span></span>
<span data-ttu-id="cd2dc-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd2dc-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd2dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2dc-138">CommonParameters</span></span>
<span data-ttu-id="cd2dc-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd2dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2dc-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2dc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2dc-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd2dc-141">INPUTS</span></span>

### <span data-ttu-id="cd2dc-142">System. Collections. Generic. list \` 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cd2dc-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cd2dc-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd2dc-143">OUTPUTS</span></span>

### <span data-ttu-id="cd2dc-144">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd2dc-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="cd2dc-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd2dc-145">NOTES</span></span>

## <span data-ttu-id="cd2dc-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd2dc-146">RELATED LINKS</span></span>

[<span data-ttu-id="cd2dc-147">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd2dc-147">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cd2dc-148">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd2dc-148">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cd2dc-149">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd2dc-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="cd2dc-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd2dc-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cd2dc-151">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd2dc-151">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


