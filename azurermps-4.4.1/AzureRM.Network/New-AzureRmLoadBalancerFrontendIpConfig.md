---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0f5db9dd785f5fdfc45bf75b4da082900a563632
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504040"
---
# <span data-ttu-id="5d403-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d403-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5d403-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d403-102">SYNOPSIS</span></span>
<span data-ttu-id="5d403-103">Előtér IP-konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="5d403-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d403-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d403-104">SYNTAX</span></span>

### <span data-ttu-id="5d403-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="5d403-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d403-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5d403-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d403-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d403-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d403-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d403-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d403-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d403-109">DESCRIPTION</span></span>
<span data-ttu-id="5d403-110">A **New-AzureRmLoadBalancerFrontendIpConfig** parancsmag az Azure-terheléselosztás előtér-IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5d403-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5d403-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5d403-111">EXAMPLES</span></span>

### <span data-ttu-id="5d403-112">1. példa: az előtér IP-konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="5d403-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="5d403-113">Az első parancs létrehoz egy MyPublicIP nevű dinamikus nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d403-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="5d403-114">A második parancs a FrontendIpConfig01 nevű előtér IP-konfigurációját a $publicip nyilvános IP-címével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5d403-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="5d403-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d403-115">PARAMETERS</span></span>

### <span data-ttu-id="5d403-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d403-116">-DefaultProfile</span></span>
<span data-ttu-id="5d403-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d403-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d403-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d403-118">-Name</span></span>
<span data-ttu-id="5d403-119">A parancsmag által létrehozott előtér IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d403-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5d403-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d403-120">-PrivateIpAddress</span></span>
<span data-ttu-id="5d403-121">A terheléselosztó privát IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d403-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="5d403-122">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="5d403-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d403-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d403-123">-PublicIpAddress</span></span>
<span data-ttu-id="5d403-124">Azt a **PublicIpAddress** objektumot adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="5d403-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d403-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5d403-125">-PublicIpAddressId</span></span>
<span data-ttu-id="5d403-126">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="5d403-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d403-127">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5d403-127">-Subnet</span></span>
<span data-ttu-id="5d403-128">Annak az **alhálózati** objektumnak a meghatározása, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="5d403-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d403-129">– NetI</span><span class="sxs-lookup"><span data-stu-id="5d403-129">-SubnetId</span></span>
<span data-ttu-id="5d403-130">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="5d403-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d403-131">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="5d403-131">-Zone</span></span>
<span data-ttu-id="5d403-132">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="5d403-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5d403-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d403-133">CommonParameters</span></span>
<span data-ttu-id="5d403-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d403-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d403-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d403-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d403-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d403-136">INPUTS</span></span>

## <span data-ttu-id="5d403-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d403-137">OUTPUTS</span></span>

### <span data-ttu-id="5d403-138">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d403-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="5d403-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d403-139">NOTES</span></span>

## <span data-ttu-id="5d403-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d403-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d403-141">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d403-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5d403-142">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d403-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5d403-143">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d403-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="5d403-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d403-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5d403-145">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d403-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


