---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 9692f44ce5d0a819d0176e0b295571ca260a2a71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843638"
---
# <span data-ttu-id="4d69e-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d69e-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4d69e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d69e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d69e-103">Az előtér IP-konfigurációjának cél állapotának beállítása a terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="4d69e-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="4d69e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d69e-104">SYNTAX</span></span>

### <span data-ttu-id="4d69e-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="4d69e-105">SetByResourceSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d69e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="4d69e-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d69e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d69e-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d69e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d69e-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d69e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d69e-109">DESCRIPTION</span></span>
<span data-ttu-id="4d69e-110">A **set-AzLoadBalancerFrontendIpConfig** parancsmag az Azure-alapú terheléselosztásban az előtér IP-konfigurációjához tartozó cél állapotot állítja be.</span><span class="sxs-lookup"><span data-stu-id="4d69e-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="4d69e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4d69e-111">EXAMPLES</span></span>

### <span data-ttu-id="4d69e-112">Példa 1: a terheléselosztó előtér IP-konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="4d69e-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="4d69e-113">Az első parancs az alhálózat nevű virtuális alhálózatot kapja, majd a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4d69e-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="4d69e-114">A második parancs megkapja a MyLoadBalancer nevű társított terheléselosztást, majd a $slb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4d69e-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="4d69e-115">A harmadik parancs a pipeline operátor segítségével átadja a terheléselosztást $slb a AzLoadBalancerFrontendIpConfig-hoz, amely egy, az $slbhoz NewFrontend nevű előtér IP-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4d69e-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="4d69e-116">A negyedik parancs átadja a terheléselosztást $slb a **set-AzLoadBalancerFrontendIpConfig** , amely az előtér IP-konfigurációját menti és frissíti.</span><span class="sxs-lookup"><span data-stu-id="4d69e-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="4d69e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d69e-117">PARAMETERS</span></span>

### <span data-ttu-id="4d69e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d69e-118">-DefaultProfile</span></span>
<span data-ttu-id="4d69e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d69e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d69e-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d69e-120">-LoadBalancer</span></span>
<span data-ttu-id="4d69e-121">A terheléselosztót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d69e-121">Specifies a load balancer.</span></span>
<span data-ttu-id="4d69e-122">Ez a parancsmag azt a cél állapotot adja meg, amely az előtér-konfigurációnak azt a kiegyenlítő konfigurációját határozza meg, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4d69e-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d69e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d69e-123">-Name</span></span>
<span data-ttu-id="4d69e-124">A beállítani kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d69e-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="4d69e-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d69e-125">-PrivateIpAddress</span></span>
<span data-ttu-id="4d69e-126">Annak a terheléselosztásnak a magánjellegű IP-címét adja meg, amely az előtér IP-konfigurációjáról van társítva.</span><span class="sxs-lookup"><span data-stu-id="4d69e-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="4d69e-127">Csak akkor adja meg ezt a paramétert, ha az *alhálózati* paramétert is meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="4d69e-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="4d69e-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d69e-128">-PublicIpAddress</span></span>
<span data-ttu-id="4d69e-129">Megadja az **PublicIpAddress** -objektumot, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="4d69e-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="4d69e-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4d69e-130">-PublicIpAddressId</span></span>
<span data-ttu-id="4d69e-131">Annak az **PublicIpAddress** -objektumnak az azonosítóját adja meg, amely a parancsmag által beállított előtér-IP-konfigurációhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="4d69e-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4d69e-132">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="4d69e-132">-Subnet</span></span>
<span data-ttu-id="4d69e-133">Azt az **alhálózati** objektumot adja meg, amely tartalmazza a parancsmag által beállított előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4d69e-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4d69e-134">– NetI</span><span class="sxs-lookup"><span data-stu-id="4d69e-134">-SubnetId</span></span>
<span data-ttu-id="4d69e-135">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amely tartalmazza a parancsmag által beállított előtér-IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4d69e-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4d69e-136">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="4d69e-136">-Zone</span></span>
<span data-ttu-id="4d69e-137">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="4d69e-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4d69e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d69e-138">CommonParameters</span></span>
<span data-ttu-id="4d69e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d69e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d69e-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d69e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d69e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d69e-141">INPUTS</span></span>

### <span data-ttu-id="4d69e-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d69e-142">PSLoadBalancer</span></span>
<span data-ttu-id="4d69e-143">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4d69e-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4d69e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d69e-144">OUTPUTS</span></span>

### <span data-ttu-id="4d69e-145">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d69e-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d69e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d69e-146">NOTES</span></span>

## <span data-ttu-id="4d69e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d69e-147">RELATED LINKS</span></span>

[<span data-ttu-id="4d69e-148">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d69e-148">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4d69e-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d69e-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4d69e-150">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d69e-150">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4d69e-151">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4d69e-151">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4d69e-152">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d69e-152">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4d69e-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d69e-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


