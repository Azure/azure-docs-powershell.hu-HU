---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493659"
---
# <span data-ttu-id="4668e-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4668e-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4668e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4668e-102">SYNOPSIS</span></span>
<span data-ttu-id="4668e-103">Az előtér IP-konfigurációját hozzáadja a terheléselosztó beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="4668e-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4668e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4668e-104">SYNTAX</span></span>

### <span data-ttu-id="4668e-105">SetByResourceSubnet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4668e-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4668e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="4668e-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4668e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4668e-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4668e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4668e-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4668e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4668e-109">DESCRIPTION</span></span>
<span data-ttu-id="4668e-110">Az **Add-AzureRmLoadBalancerFrontendIpConifg** parancsmag egy előtér-IP-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="4668e-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4668e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4668e-111">EXAMPLES</span></span>

### <span data-ttu-id="4668e-112">Példa: az előtér IP-konfigurációjának hozzáadása dinamikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="4668e-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4668e-113">Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzureRmVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="4668e-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="4668e-114">A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4668e-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="4668e-115">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzureRmLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, a $MySubnet nevű változóban tárolt dinamikus magánhálózati IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="4668e-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="4668e-116">Példa 2 az előtér IP-konfigurációjának hozzáadása statikus IP-címmel</span><span class="sxs-lookup"><span data-stu-id="4668e-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4668e-117">Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzureRmVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="4668e-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="4668e-118">A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4668e-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="4668e-119">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzureRmLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, az $subnet nevű változóban tárolt statikus magánhálózati IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="4668e-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="4668e-120">Példa 3 előtér IP-konfigurációjának hozzáadása nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="4668e-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4668e-121">Az első parancs a MyPub nevű Azure nyilvános IP-címet kapja, és az eredményt az $PublicIp nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4668e-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="4668e-122">A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzureRmLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz az $PublicIp nevű változóban tárolt nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="4668e-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="4668e-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4668e-123">PARAMETERS</span></span>

### <span data-ttu-id="4668e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4668e-124">-DefaultProfile</span></span>
<span data-ttu-id="4668e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4668e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4668e-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4668e-126">-LoadBalancer</span></span>
<span data-ttu-id="4668e-127">Egy **LoadBalancer** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4668e-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4668e-128">Ez a parancsmag az előtér IP-konfigurációját hozzáadja a paraméter által megadott terheléselosztó típushoz.</span><span class="sxs-lookup"><span data-stu-id="4668e-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4668e-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4668e-129">-Name</span></span>
<span data-ttu-id="4668e-130">A hozzáadni kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4668e-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="4668e-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4668e-131">-PrivateIpAddress</span></span>
<span data-ttu-id="4668e-132">Annak a magánhálózati IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="4668e-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4668e-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4668e-133">-PublicIpAddress</span></span>
<span data-ttu-id="4668e-134">Annak a nyilvános IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="4668e-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4668e-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4668e-135">-PublicIpAddressId</span></span>
<span data-ttu-id="4668e-136">Specifes annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4668e-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4668e-137">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="4668e-137">-Subnet</span></span>
<span data-ttu-id="4668e-138">Annak az alhálózati objektumnak a meghatározása, amelyben az előtér-IP-konfigurációt fel szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="4668e-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4668e-139">– NetI</span><span class="sxs-lookup"><span data-stu-id="4668e-139">-SubnetId</span></span>
<span data-ttu-id="4668e-140">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4668e-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4668e-141">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="4668e-141">-Zone</span></span>
<span data-ttu-id="4668e-142">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="4668e-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4668e-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4668e-143">-Confirm</span></span>
<span data-ttu-id="4668e-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4668e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4668e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4668e-145">-WhatIf</span></span>
<span data-ttu-id="4668e-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4668e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4668e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4668e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4668e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4668e-148">CommonParameters</span></span>
<span data-ttu-id="4668e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4668e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4668e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4668e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4668e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4668e-151">INPUTS</span></span>

### <span data-ttu-id="4668e-152">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4668e-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4668e-153">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4668e-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="4668e-154">System. Collections. Generic. list \` 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4668e-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4668e-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4668e-155">OUTPUTS</span></span>

### <span data-ttu-id="4668e-156">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4668e-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4668e-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4668e-157">NOTES</span></span>

## <span data-ttu-id="4668e-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4668e-158">RELATED LINKS</span></span>

[<span data-ttu-id="4668e-159">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4668e-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4668e-160">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4668e-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="4668e-161">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4668e-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4668e-162">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4668e-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4668e-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4668e-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4668e-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4668e-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


