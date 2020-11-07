---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 128621265766f921a2c7b052f4fe276c8f67e03f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837805"
---
# <span data-ttu-id="e2be2-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2be2-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="e2be2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2be2-102">SYNOPSIS</span></span>
<span data-ttu-id="e2be2-103">Egy előtér IP-címének konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="e2be2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2be2-104">SYNTAX</span></span>

### <span data-ttu-id="e2be2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2be2-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2be2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2be2-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2be2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2be2-107">DESCRIPTION</span></span>
<span data-ttu-id="e2be2-108">A **set-AzApplicationGatewayFrontendIPConfig** parancsmag frissíti az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e2be2-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="e2be2-109">Az alkalmazás-átjárók kétféle előtér-IP-címet támogatnak:</span><span class="sxs-lookup"><span data-stu-id="e2be2-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="e2be2-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="e2be2-110">Public IP addresses</span></span>
- <span data-ttu-id="e2be2-111">Privát IP-címek, amelyek esetében a konfiguráció belső terheléselosztást (ILB) használ, az alkalmazás-átjárók legfeljebb egy nyilvános IP-címen és egy privát IP-címen lehetnek.</span><span class="sxs-lookup"><span data-stu-id="e2be2-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="e2be2-112">A nyilvános IP-címet és a privát IP-címet külön-külön kell hozzáadni az első végpont IP-címeihez.</span><span class="sxs-lookup"><span data-stu-id="e2be2-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="e2be2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e2be2-113">EXAMPLES</span></span>

### <span data-ttu-id="e2be2-114">1. példa: nyilvános IP beállítása az alkalmazás-átjárók előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="e2be2-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="e2be2-115">Az első parancs létrehozza a nyilvános IP-cím objektumot, és a $PublicIp változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="e2be2-116">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2be2-117">A harmadik parancs frissíti a FrontEndIp01 nevű előtér-IP-konfigurációt az $AppGw átjáróhoz az $PublicIp tárolt cím használatával.</span><span class="sxs-lookup"><span data-stu-id="e2be2-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="e2be2-118">2. példa: statikus privát IP beállítása az alkalmazás-átjárók előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="e2be2-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="e2be2-119">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e2be2-120">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e2be2-121">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2be2-122">A negyedik parancs hozzáadja a FrontendIP02 nevű előtér-IP-konfigurációt $Subnet a második parancsból és a privát IP-cím 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="e2be2-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="e2be2-123">3. példa: a Dynamic Private IP beállítása az alkalmazás átjárójának előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="e2be2-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="e2be2-124">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e2be2-125">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e2be2-126">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2be2-127">A negyedik parancs a második parancs segítségével felveszi a FrontendIP02 nevű előtér-IP-konfigurációt a $Subnet használatával.</span><span class="sxs-lookup"><span data-stu-id="e2be2-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="e2be2-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2be2-128">PARAMETERS</span></span>

### <span data-ttu-id="e2be2-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2be2-129">-ApplicationGateway</span></span>
<span data-ttu-id="e2be2-130">Itt adhatja meg azt az Application Gateway-objektumot, amelybe az előtér IP-konfigurációját módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="e2be2-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2be2-131">-DefaultProfile</span></span>
<span data-ttu-id="e2be2-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2be2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2be2-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2be2-133">-Name</span></span>
<span data-ttu-id="e2be2-134">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="e2be2-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e2be2-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="e2be2-135">-PrivateIPAddress</span></span>
<span data-ttu-id="e2be2-136">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2be2-136">Specifies the private IP address.</span></span>
<span data-ttu-id="e2be2-137">Ha meg van adva, az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="e2be2-137">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="e2be2-138">-PublicIPAddress</span></span>
<span data-ttu-id="e2be2-139">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="e2be2-139">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="e2be2-140">-PublicIPAddressId</span></span>
<span data-ttu-id="e2be2-141">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2be2-141">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-142">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="e2be2-142">-Subnet</span></span>
<span data-ttu-id="e2be2-143">Azt az alhálózatot adja meg, amely az alkalmazás átjáróját használja.</span><span class="sxs-lookup"><span data-stu-id="e2be2-143">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="e2be2-144">Adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="e2be2-144">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="e2be2-145">Ha a *PrivateIPAddress* cím meg van adva, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="e2be2-145">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="e2be2-146">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e2be2-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-147">– NetI</span><span class="sxs-lookup"><span data-stu-id="e2be2-147">-SubnetId</span></span>
<span data-ttu-id="e2be2-148">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2be2-148">Specifies the subnet ID.</span></span>
<span data-ttu-id="e2be2-149">Adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="e2be2-149">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="e2be2-150">Ha a *PrivateIPAddress* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="e2be2-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="e2be2-151">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e2be2-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2be2-152">CommonParameters</span></span>
<span data-ttu-id="e2be2-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2be2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2be2-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2be2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2be2-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2be2-155">INPUTS</span></span>

### <span data-ttu-id="e2be2-156">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2be2-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2be2-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2be2-157">OUTPUTS</span></span>

### <span data-ttu-id="e2be2-158">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2be2-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2be2-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2be2-159">NOTES</span></span>

## <span data-ttu-id="e2be2-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2be2-160">RELATED LINKS</span></span>

[<span data-ttu-id="e2be2-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2be2-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e2be2-162">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2be2-162">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e2be2-163">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2be2-163">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e2be2-164">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2be2-164">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e2be2-165">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2be2-165">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


