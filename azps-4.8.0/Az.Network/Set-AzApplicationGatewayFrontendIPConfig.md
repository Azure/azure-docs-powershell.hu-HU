---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182976"
---
# <span data-ttu-id="d9902-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d9902-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="d9902-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9902-102">SYNOPSIS</span></span>
<span data-ttu-id="d9902-103">Egy előtér IP-címének konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="d9902-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="d9902-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9902-104">SYNTAX</span></span>

### <span data-ttu-id="d9902-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9902-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9902-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d9902-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9902-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9902-107">DESCRIPTION</span></span>
<span data-ttu-id="d9902-108">A **set-AzApplicationGatewayFrontendIPConfig** parancsmag frissíti az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d9902-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="d9902-109">Az alkalmazás-átjárók kétféle előtér-IP-címet támogatnak:</span><span class="sxs-lookup"><span data-stu-id="d9902-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="d9902-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="d9902-110">Public IP addresses</span></span>
- <span data-ttu-id="d9902-111">Privát IP-címek, amelyek esetében a konfiguráció belső terheléselosztást (ILB) használ, az alkalmazás-átjárók legfeljebb egy nyilvános IP-címen és egy privát IP-címen lehetnek.</span><span class="sxs-lookup"><span data-stu-id="d9902-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="d9902-112">A nyilvános IP-címet és a privát IP-címet külön-külön kell hozzáadni az első végpont IP-címeihez.</span><span class="sxs-lookup"><span data-stu-id="d9902-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="d9902-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d9902-113">EXAMPLES</span></span>

### <span data-ttu-id="d9902-114">1. példa: nyilvános IP beállítása az alkalmazás-átjárók előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="d9902-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="d9902-115">Az első parancs létrehozza a nyilvános IP-cím objektumot, és a $PublicIp változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="d9902-116">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d9902-117">A harmadik parancs frissíti a FrontEndIp01 nevű előtér-IP-konfigurációt az $AppGw átjáróhoz az $PublicIp tárolt cím használatával.</span><span class="sxs-lookup"><span data-stu-id="d9902-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="d9902-118">2. példa: statikus privát IP beállítása az alkalmazás-átjárók előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="d9902-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="d9902-119">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="d9902-120">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="d9902-121">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d9902-122">A negyedik parancs hozzáadja a FrontendIP02 nevű előtér-IP-konfigurációt $Subnet a második parancsból és a privát IP-cím 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="d9902-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="d9902-123">3. példa: a Dynamic Private IP beállítása az alkalmazás átjárójának előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="d9902-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="d9902-124">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="d9902-125">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="d9902-126">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9902-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d9902-127">A negyedik parancs a második parancs segítségével felveszi a FrontendIP02 nevű előtér-IP-konfigurációt a $Subnet használatával.</span><span class="sxs-lookup"><span data-stu-id="d9902-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="d9902-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9902-128">PARAMETERS</span></span>

### <span data-ttu-id="d9902-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9902-129">-ApplicationGateway</span></span>
<span data-ttu-id="d9902-130">Itt adhatja meg azt az Application Gateway-objektumot, amelybe az előtér IP-konfigurációját módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="d9902-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9902-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9902-131">-DefaultProfile</span></span>
<span data-ttu-id="d9902-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9902-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9902-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9902-133">-Name</span></span>
<span data-ttu-id="d9902-134">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="d9902-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d9902-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="d9902-135">-PrivateIPAddress</span></span>
<span data-ttu-id="d9902-136">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9902-136">Specifies the private IP address.</span></span>
<span data-ttu-id="d9902-137">Ha meg van adva, az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="d9902-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="d9902-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9902-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="d9902-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9902-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="d9902-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d9902-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="d9902-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d9902-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="d9902-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="d9902-142">-PublicIPAddress</span></span>
<span data-ttu-id="d9902-143">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="d9902-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="d9902-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="d9902-144">-PublicIPAddressId</span></span>
<span data-ttu-id="d9902-145">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9902-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="d9902-146">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="d9902-146">-Subnet</span></span>
<span data-ttu-id="d9902-147">Azt az alhálózatot adja meg, amely az alkalmazás átjáróját használja.</span><span class="sxs-lookup"><span data-stu-id="d9902-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="d9902-148">Adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="d9902-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="d9902-149">Ha a *PrivateIPAddress* cím meg van adva, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="d9902-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="d9902-150">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="d9902-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d9902-151">– NetI</span><span class="sxs-lookup"><span data-stu-id="d9902-151">-SubnetId</span></span>
<span data-ttu-id="d9902-152">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9902-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="d9902-153">Adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="d9902-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="d9902-154">Ha a *PrivateIPAddress* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="d9902-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="d9902-155">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="d9902-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d9902-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9902-156">CommonParameters</span></span>
<span data-ttu-id="d9902-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9902-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9902-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d9902-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9902-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9902-159">INPUTS</span></span>

### <span data-ttu-id="d9902-160">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9902-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9902-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9902-161">OUTPUTS</span></span>

### <span data-ttu-id="d9902-162">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9902-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9902-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9902-163">NOTES</span></span>

## <span data-ttu-id="d9902-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9902-164">RELATED LINKS</span></span>

[<span data-ttu-id="d9902-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d9902-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d9902-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d9902-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d9902-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d9902-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d9902-168">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d9902-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d9902-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d9902-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


