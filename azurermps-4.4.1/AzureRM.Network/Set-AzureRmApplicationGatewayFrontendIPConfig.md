---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1abb59c6f610182e14bdf9483610cdb9bbbb66bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680852"
---
# <span data-ttu-id="5cb57-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5cb57-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="5cb57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cb57-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb57-103">Egy előtér IP-címének konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cb57-104">SYNTAX</span></span>

### <span data-ttu-id="5cb57-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb57-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cb57-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5cb57-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cb57-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cb57-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb57-108">A **set-AzureRmApplicationGatewayFrontendIPConfig** parancsmag frissíti az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5cb57-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="5cb57-109">Az alkalmazás-átjárók kétféle előtér-IP-címet támogatnak:</span><span class="sxs-lookup"><span data-stu-id="5cb57-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="5cb57-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="5cb57-110">Public IP addresses</span></span>
- <span data-ttu-id="5cb57-111">Privát IP-címek, amelyekhez a konfiguráció belső terheléselosztást használ (ILB)</span><span class="sxs-lookup"><span data-stu-id="5cb57-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="5cb57-112">Az alkalmazás-átjárók legfeljebb egy nyilvános IP-címet és egy privát IP-címet tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="5cb57-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="5cb57-113">A nyilvános IP-címet és a privát IP-címet külön-külön kell hozzáadni az első végpont IP-címeihez.</span><span class="sxs-lookup"><span data-stu-id="5cb57-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="5cb57-114">Példák</span><span class="sxs-lookup"><span data-stu-id="5cb57-114">EXAMPLES</span></span>

### <span data-ttu-id="5cb57-115">1. példa: nyilvános IP beállítása az alkalmazás-átjárók előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="5cb57-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="5cb57-116">Az első parancs létrehozza a nyilvános IP-cím objektumot, és a $PublicIp változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="5cb57-117">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5cb57-118">A harmadik parancs frissíti a FrontEndIp01 nevű előtér-IP-konfigurációt az $AppGw átjáróhoz az $PublicIp tárolt cím használatával.</span><span class="sxs-lookup"><span data-stu-id="5cb57-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="5cb57-119">2. példa: statikus privát IP beállítása az alkalmazás-átjárók előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="5cb57-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="5cb57-120">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="5cb57-121">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="5cb57-122">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5cb57-123">A negyedik parancs hozzáadja a FrontendIP02 nevű előtér-IP-konfigurációt $Subnet a második parancsból és a privát IP-cím 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="5cb57-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="5cb57-124">3. példa: a Dynamic Private IP beállítása az alkalmazás átjárójának előtér-IP-címéhez</span><span class="sxs-lookup"><span data-stu-id="5cb57-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="5cb57-125">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="5cb57-126">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="5cb57-127">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5cb57-128">A negyedik parancs a második parancs segítségével felveszi a FrontendIP02 nevű előtér-IP-konfigurációt a $Subnet használatával.</span><span class="sxs-lookup"><span data-stu-id="5cb57-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="5cb57-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cb57-129">PARAMETERS</span></span>

### <span data-ttu-id="5cb57-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cb57-130">-ApplicationGateway</span></span>
<span data-ttu-id="5cb57-131">Itt adhatja meg azt az Application Gateway-objektumot, amelybe az előtér IP-konfigurációját módosítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="5cb57-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="5cb57-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5cb57-132">-Name</span></span>
<span data-ttu-id="5cb57-133">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="5cb57-133">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5cb57-134">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="5cb57-134">-PrivateIPAddress</span></span>
<span data-ttu-id="5cb57-135">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb57-135">Specifies the private IP address.</span></span>
<span data-ttu-id="5cb57-136">Ha meg van adva, az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="5cb57-136">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="5cb57-137">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="5cb57-137">-PublicIPAddress</span></span>
<span data-ttu-id="5cb57-138">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="5cb57-138">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="5cb57-139">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="5cb57-139">-PublicIPAddressId</span></span>
<span data-ttu-id="5cb57-140">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb57-140">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="5cb57-141">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5cb57-141">-Subnet</span></span>
<span data-ttu-id="5cb57-142">Azt az alhálózatot adja meg, amely az alkalmazás átjáróját használja.</span><span class="sxs-lookup"><span data-stu-id="5cb57-142">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="5cb57-143">Adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="5cb57-143">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="5cb57-144">Ha a *PrivateIPAddress* cím meg van adva, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="5cb57-144">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="5cb57-145">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5cb57-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="5cb57-146">– NetI</span><span class="sxs-lookup"><span data-stu-id="5cb57-146">-SubnetId</span></span>
<span data-ttu-id="5cb57-147">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb57-147">Specifies the subnet ID.</span></span>
<span data-ttu-id="5cb57-148">Adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="5cb57-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="5cb57-149">Ha a *PrivateIPAddress* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="5cb57-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="5cb57-150">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5cb57-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="5cb57-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb57-151">-DefaultProfile</span></span>
<span data-ttu-id="5cb57-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cb57-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cb57-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb57-153">CommonParameters</span></span>
<span data-ttu-id="5cb57-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cb57-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb57-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb57-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb57-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cb57-156">INPUTS</span></span>

### <span data-ttu-id="5cb57-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5cb57-157">System.String</span></span>

## <span data-ttu-id="5cb57-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cb57-158">OUTPUTS</span></span>

### <span data-ttu-id="5cb57-159">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cb57-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5cb57-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cb57-160">NOTES</span></span>

## <span data-ttu-id="5cb57-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cb57-161">RELATED LINKS</span></span>

[<span data-ttu-id="5cb57-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5cb57-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5cb57-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5cb57-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5cb57-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5cb57-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5cb57-165">Új – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5cb57-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5cb57-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5cb57-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


