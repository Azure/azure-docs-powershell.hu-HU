---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d071e6f20d91dacfd99ca9566c64c4734ae93e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494820"
---
# <span data-ttu-id="18839-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18839-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="18839-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18839-102">SYNOPSIS</span></span>
<span data-ttu-id="18839-103">Az előtér IP-konfigurációjának cél állapotának beállítása a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="18839-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18839-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18839-104">SYNTAX</span></span>

### <span data-ttu-id="18839-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="18839-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18839-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="18839-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18839-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18839-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18839-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18839-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18839-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="18839-109">DESCRIPTION</span></span>
<span data-ttu-id="18839-110">A **set-AzureRmLoadBalancerFrontendIpConfig** parancsmag az Azure-alapú terheléselosztásban az előtér IP-konfigurációjához tartozó cél állapotot állítja be.</span><span class="sxs-lookup"><span data-stu-id="18839-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="18839-111">Példák</span><span class="sxs-lookup"><span data-stu-id="18839-111">EXAMPLES</span></span>

### <span data-ttu-id="18839-112">Példa 1: a terheléselosztó előtér IP-konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="18839-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="18839-113">Az első parancs az alhálózat nevű virtuális alhálózatot kapja, majd a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18839-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="18839-114">A második parancs megkapja a MyLoadBalancer nevű társított terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18839-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="18839-115">A harmadik parancs a pipeline operátor segítségével átadja a terheléselosztást $slb a AzureRmLoadBalancerFrontendIpConfig-hoz, amely egy, az $slbhoz NewFrontend nevű előtér IP-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="18839-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="18839-116">A negyedik parancs átadja a terheléselosztást $slb a **set-AzureRmLoadBalancerFrontendIpConfig** , amely az előtér IP-konfigurációját menti és frissíti.</span><span class="sxs-lookup"><span data-stu-id="18839-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="18839-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18839-117">PARAMETERS</span></span>

### <span data-ttu-id="18839-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18839-118">-DefaultProfile</span></span>
<span data-ttu-id="18839-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18839-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18839-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18839-120">-LoadBalancer</span></span>
<span data-ttu-id="18839-121">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="18839-121">Specifies a load balancer.</span></span>
<span data-ttu-id="18839-122">Ez a parancsmag azt a cél állapotot adja meg, amely az előtér-konfigurációnak azt a kiegyenlítő konfigurációját határozza meg, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="18839-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18839-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18839-123">-Name</span></span>
<span data-ttu-id="18839-124">A beállítani kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18839-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="18839-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="18839-125">-PrivateIpAddress</span></span>
<span data-ttu-id="18839-126">Annak a terheléselosztásnak a magánjellegű IP-címét adja meg, amely az előtér IP-konfigurációjáról van társítva.</span><span class="sxs-lookup"><span data-stu-id="18839-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="18839-127">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="18839-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="18839-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18839-128">-PublicIpAddress</span></span>
<span data-ttu-id="18839-129">Megadja az **PublicIpAddress** -objektumot, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="18839-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="18839-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="18839-130">-PublicIpAddressId</span></span>
<span data-ttu-id="18839-131">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amely a parancsmag által beállított előtér-IP-konfigurációhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="18839-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="18839-132">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="18839-132">-Subnet</span></span>
<span data-ttu-id="18839-133">Azt az **alhálózati** objektumot adja meg, amely tartalmazza a parancsmag által beállított előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="18839-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="18839-134">– NetI</span><span class="sxs-lookup"><span data-stu-id="18839-134">-SubnetId</span></span>
<span data-ttu-id="18839-135">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amely tartalmazza a parancsmag által beállított előtér-IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="18839-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="18839-136">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="18839-136">-Zone</span></span>
<span data-ttu-id="18839-137">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="18839-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="18839-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18839-138">CommonParameters</span></span>
<span data-ttu-id="18839-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18839-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18839-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18839-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18839-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18839-141">INPUTS</span></span>

### <span data-ttu-id="18839-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18839-142">PSLoadBalancer</span></span>
<span data-ttu-id="18839-143">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="18839-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="18839-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18839-144">OUTPUTS</span></span>

### <span data-ttu-id="18839-145">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18839-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="18839-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18839-146">NOTES</span></span>

## <span data-ttu-id="18839-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18839-147">RELATED LINKS</span></span>

[<span data-ttu-id="18839-148">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18839-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="18839-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18839-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="18839-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18839-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="18839-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="18839-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="18839-152">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18839-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="18839-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18839-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


