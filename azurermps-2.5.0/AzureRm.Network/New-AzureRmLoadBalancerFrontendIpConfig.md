---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 3cd241b84f7ac03dc268a8f04df0490f6a9f9665
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850386"
---
# <span data-ttu-id="1f056-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f056-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1f056-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f056-102">SYNOPSIS</span></span>
<span data-ttu-id="1f056-103">Előtér IP-konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="1f056-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f056-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f056-104">SYNTAX</span></span>

### <span data-ttu-id="1f056-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="1f056-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f056-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="1f056-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f056-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f056-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f056-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f056-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f056-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f056-109">DESCRIPTION</span></span>
<span data-ttu-id="1f056-110">A **New-AzureRmLoadBalancerFrontendIpConfig** parancsmag az Azure-terheléselosztás előtér-IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f056-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1f056-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1f056-111">EXAMPLES</span></span>

### <span data-ttu-id="1f056-112">1. példa: az előtér IP-konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="1f056-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="1f056-113">Az első parancs létrehoz egy MyPublicIP nevű dinamikus nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1f056-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="1f056-114">A második parancs a FrontendIpConfig01 nevű előtér IP-konfigurációját a $publicip nyilvános IP-címével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f056-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="1f056-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f056-115">PARAMETERS</span></span>

### <span data-ttu-id="1f056-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f056-116">-DefaultProfile</span></span>
<span data-ttu-id="1f056-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f056-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f056-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f056-118">-Name</span></span>
<span data-ttu-id="1f056-119">A parancsmag által létrehozott előtér IP-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f056-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f056-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f056-120">-PrivateIpAddress</span></span>
<span data-ttu-id="1f056-121">A terheléselosztó privát IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f056-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="1f056-122">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="1f056-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f056-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f056-123">-PublicIpAddress</span></span>
<span data-ttu-id="1f056-124">Azt a **PublicIpAddress** objektumot adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="1f056-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f056-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="1f056-125">-PublicIpAddressId</span></span>
<span data-ttu-id="1f056-126">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="1f056-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f056-127">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="1f056-127">-Subnet</span></span>
<span data-ttu-id="1f056-128">Annak az **alhálózati** objektumnak a meghatározása, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="1f056-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f056-129">– NetI</span><span class="sxs-lookup"><span data-stu-id="1f056-129">-SubnetId</span></span>
<span data-ttu-id="1f056-130">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben előtér-IP-konfiguráció hozható létre.</span><span class="sxs-lookup"><span data-stu-id="1f056-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f056-131">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="1f056-131">-Zone</span></span>
<span data-ttu-id="1f056-132">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="1f056-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="1f056-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f056-133">CommonParameters</span></span>
<span data-ttu-id="1f056-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f056-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f056-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f056-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f056-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f056-136">INPUTS</span></span>

## <span data-ttu-id="1f056-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f056-137">OUTPUTS</span></span>

### <span data-ttu-id="1f056-138">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f056-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="1f056-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f056-139">NOTES</span></span>

## <span data-ttu-id="1f056-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f056-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f056-141">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f056-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f056-142">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f056-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f056-143">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f056-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1f056-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f056-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f056-145">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f056-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


