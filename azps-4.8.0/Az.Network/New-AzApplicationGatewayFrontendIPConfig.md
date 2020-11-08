---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181591"
---
# <span data-ttu-id="5ca68-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5ca68-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="5ca68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ca68-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca68-103">Előtér IP-konfigurációját hozza létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5ca68-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="5ca68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ca68-104">SYNTAX</span></span>

### <span data-ttu-id="5ca68-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca68-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca68-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5ca68-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca68-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ca68-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca68-108">A **New-AzApplicationGatewayFrontendIPConfig** parancsmag előtér-IP-konfigurációt hoz létre az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="5ca68-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="5ca68-109">Az alkalmazás-átjárók kétféle előtér-IP-konfigurációt támogatnak:</span><span class="sxs-lookup"><span data-stu-id="5ca68-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="5ca68-110">Nyilvános IP-címek – privát IP-címek belső terheléselosztási (ILB) használatával.</span><span class="sxs-lookup"><span data-stu-id="5ca68-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="5ca68-111">Az alkalmazás-átjárók legfeljebb egy nyilvános IP-címet és egy privát IP-címet tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="5ca68-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="5ca68-112">A nyilvános IP-címet és a privát IP-címet külön-külön kell hozzáadni az előtér-IP-címekhez.</span><span class="sxs-lookup"><span data-stu-id="5ca68-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="5ca68-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5ca68-113">EXAMPLES</span></span>

### <span data-ttu-id="5ca68-114">Példa 1: előtér IP-konfigurációjának létrehozása nyilvános IP-erőforrás-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="5ca68-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="5ca68-115">Az első parancs létrehoz egy nyilvános IP-erőforrás-objektumot, és a $PublicIP változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="5ca68-116">A második parancs $PublicIP segítségével létrehoz egy FrontEndIP01 nevű új előtér-IP-konfigurációt, és a $FrontEnd változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="5ca68-117">2. példa: statikus privát IP létrehozása előtér-IP-címként</span><span class="sxs-lookup"><span data-stu-id="5ca68-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="5ca68-118">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="5ca68-119">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="5ca68-120">A harmadik parancs létrehozza a $Subnet FrontEndIP02 nevű előtér-IP-konfigurációt a második parancs és a privát IP-cím 10.0.1.1, majd a $FrontEnd változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="5ca68-121">3. példa: dinamikus privát IP-cím létrehozása előtér-IP-címként</span><span class="sxs-lookup"><span data-stu-id="5ca68-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="5ca68-122">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="5ca68-123">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="5ca68-124">A harmadik parancs a második parancs segítségével létrehoz egy FrontEndIP03 nevű előtér-IP-konfigurációt, és a $FrontEnd változóban tárolja a $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5ca68-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="5ca68-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ca68-125">PARAMETERS</span></span>

### <span data-ttu-id="5ca68-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca68-126">-DefaultProfile</span></span>
<span data-ttu-id="5ca68-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ca68-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ca68-128">-Name</span></span>
<span data-ttu-id="5ca68-129">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5ca68-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ca68-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="5ca68-130">-PrivateIPAddress</span></span>
<span data-ttu-id="5ca68-131">Annak a magánhálózati IP-címnek a megadása, amelyhez ez a parancsmag társítva van az alkalmazás-átjáró előtér IP-címével.</span><span class="sxs-lookup"><span data-stu-id="5ca68-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="5ca68-132">Ez csak akkor adható meg, ha meg van adva alhálózat.</span><span class="sxs-lookup"><span data-stu-id="5ca68-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="5ca68-133">Az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="5ca68-133">This IP is statically allocated from the subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ca68-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="5ca68-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ca68-135">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5ca68-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="5ca68-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5ca68-137">PrivateLinkConfigurationId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="5ca68-138">-PublicIPAddress</span></span>
<span data-ttu-id="5ca68-139">Annak a nyilvános IP-cím objektumnak a meghatározása, amelyet ez a parancsmag társít az alkalmazás átjárójának előtér-IP-címéhez.</span><span class="sxs-lookup"><span data-stu-id="5ca68-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="5ca68-140">-PublicIPAddressId</span></span>
<span data-ttu-id="5ca68-141">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amely a parancsmag a program átjárójának előtér-IP-címéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="5ca68-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-142">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5ca68-142">-Subnet</span></span>
<span data-ttu-id="5ca68-143">Annak az alhálózatnak az objektumát adja meg, amely a parancsmag a program átjárójának előtér-IP-címéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="5ca68-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="5ca68-144">Ha megadja ezt a paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="5ca68-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="5ca68-145">Ha a *PrivateIPAddress* paramétert adja meg, akkor az a paraméter által meghatározott alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="5ca68-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="5ca68-146">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5ca68-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-147">– NetI</span><span class="sxs-lookup"><span data-stu-id="5ca68-147">-SubnetId</span></span>
<span data-ttu-id="5ca68-148">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag az alkalmazás-átjáró előtér-IP-konfigurációját társítja.</span><span class="sxs-lookup"><span data-stu-id="5ca68-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="5ca68-149">Ha megadja az *alhálózati* paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="5ca68-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="5ca68-150">Ha a *PrivateIPAddress* paramétert adja meg, akkor az *alhálózat* által megadott alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="5ca68-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="5ca68-151">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5ca68-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca68-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca68-152">CommonParameters</span></span>
<span data-ttu-id="5ca68-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ca68-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca68-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ca68-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca68-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca68-155">INPUTS</span></span>

### <span data-ttu-id="5ca68-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="5ca68-156">None</span></span>

## <span data-ttu-id="5ca68-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca68-157">OUTPUTS</span></span>

### <span data-ttu-id="5ca68-158">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ca68-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="5ca68-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ca68-159">NOTES</span></span>

## <span data-ttu-id="5ca68-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ca68-160">RELATED LINKS</span></span>

[<span data-ttu-id="5ca68-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5ca68-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5ca68-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5ca68-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5ca68-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5ca68-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5ca68-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5ca68-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


