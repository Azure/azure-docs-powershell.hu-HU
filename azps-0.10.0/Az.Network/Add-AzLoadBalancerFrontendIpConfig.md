---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 80324e1d6fa87959edb0da8e7aa72f3b2a42a3b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841830"
---
# <span data-ttu-id="2cf1a-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2cf1a-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="2cf1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf1a-103">Az előtér IP-konfigurációját hozzáadja a terheléselosztó beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="2cf1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cf1a-104">SYNTAX</span></span>

### <span data-ttu-id="2cf1a-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="2cf1a-105">SetByResourceSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf1a-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="2cf1a-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf1a-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cf1a-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf1a-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cf1a-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf1a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cf1a-109">DESCRIPTION</span></span>
<span data-ttu-id="2cf1a-110">Az **Add-AzLoadBalancerFrontendIpConifg** parancsmag egy előtér-IP-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="2cf1a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2cf1a-111">EXAMPLES</span></span>

### <span data-ttu-id="2cf1a-112">Példa: az előtér IP-konfigurációjának hozzáadása dinamikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="2cf1a-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="2cf1a-113">Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="2cf1a-114">A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="2cf1a-115">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, a $MySubnet nevű változóban tárolt dinamikus magánhálózati IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="2cf1a-116">Példa 2 az előtér IP-konfigurációjának hozzáadása statikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="2cf1a-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="2cf1a-117">Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="2cf1a-118">A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="2cf1a-119">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, az $subnet nevű változóban tárolt statikus magánhálózati IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="2cf1a-120">Példa 3 előtér IP-konfigurációjának hozzáadása nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="2cf1a-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="2cf1a-121">Az első parancs a MyPub nevű Azure nyilvános IP-címet kapja, és az eredményt az $PublicIp nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="2cf1a-122">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz az $PublicIp nevű változóban tárolt nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="2cf1a-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cf1a-123">PARAMETERS</span></span>

### <span data-ttu-id="2cf1a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf1a-124">-DefaultProfile</span></span>
<span data-ttu-id="2cf1a-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf1a-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cf1a-126">-LoadBalancer</span></span>
<span data-ttu-id="2cf1a-127">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="2cf1a-128">Ez a parancsmag az előtér IP-konfigurációját hozzáadja a paraméter által megadott terheléselosztó típushoz.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2cf1a-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2cf1a-129">-Name</span></span>
<span data-ttu-id="2cf1a-130">A hozzáadni kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="2cf1a-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cf1a-131">-PrivateIpAddress</span></span>
<span data-ttu-id="2cf1a-132">Annak a magánhálózati IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cf1a-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cf1a-133">-PublicIpAddress</span></span>
<span data-ttu-id="2cf1a-134">Annak a nyilvános IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cf1a-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2cf1a-135">-PublicIpAddressId</span></span>
<span data-ttu-id="2cf1a-136">Specifes annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cf1a-137">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="2cf1a-137">-Subnet</span></span>
<span data-ttu-id="2cf1a-138">Annak az alhálózati objektumnak a meghatározása, amelyben az előtér-IP-konfigurációt fel szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cf1a-139">– NetI</span><span class="sxs-lookup"><span data-stu-id="2cf1a-139">-SubnetId</span></span>
<span data-ttu-id="2cf1a-140">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cf1a-141">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="2cf1a-141">-Zone</span></span>
<span data-ttu-id="2cf1a-142">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="2cf1a-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2cf1a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf1a-143">CommonParameters</span></span>
<span data-ttu-id="2cf1a-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cf1a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf1a-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf1a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf1a-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf1a-146">INPUTS</span></span>

### <span data-ttu-id="2cf1a-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cf1a-147">PSLoadBalancer</span></span>
<span data-ttu-id="2cf1a-148">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2cf1a-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2cf1a-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf1a-149">OUTPUTS</span></span>

### <span data-ttu-id="2cf1a-150">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2cf1a-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2cf1a-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cf1a-151">NOTES</span></span>

## <span data-ttu-id="2cf1a-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cf1a-152">RELATED LINKS</span></span>

[<span data-ttu-id="2cf1a-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2cf1a-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2cf1a-154">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2cf1a-154">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="2cf1a-155">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2cf1a-155">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2cf1a-156">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2cf1a-156">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2cf1a-157">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2cf1a-157">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2cf1a-158">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2cf1a-158">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


