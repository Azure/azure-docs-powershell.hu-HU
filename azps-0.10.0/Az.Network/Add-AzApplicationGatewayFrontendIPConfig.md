---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 4b0fd2fd55b255a9734a0c6b0c325f7ac113b4e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841881"
---
# <span data-ttu-id="e4441-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e4441-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="e4441-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4441-102">SYNOPSIS</span></span>
<span data-ttu-id="e4441-103">Az előtér IP-konfigurációját hozzáadja egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e4441-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="e4441-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4441-104">SYNTAX</span></span>

### <span data-ttu-id="e4441-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4441-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4441-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e4441-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4441-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4441-107">DESCRIPTION</span></span>
<span data-ttu-id="e4441-108">Az **Add-AzApplicationGatewayFrontendIPConfig** parancsmag egyoldalas IP-konfigurációt ad az alkalmazás-átjárónak.</span><span class="sxs-lookup"><span data-stu-id="e4441-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="e4441-109">Az alkalmazás-átjárók kétféle előtér-IP-konfigurációt támogatnak:</span><span class="sxs-lookup"><span data-stu-id="e4441-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="e4441-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="e4441-110">Public IP addresses</span></span>
- <span data-ttu-id="e4441-111">Privát IP-címek belső terheléselosztási (ILB) használatával</span><span class="sxs-lookup"><span data-stu-id="e4441-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="e4441-112">Az alkalmazás-átjárók legfeljebb egy nyilvános IP-címet és egy privát IP-t tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="e4441-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="e4441-113">Adja meg a nyilvános IP-címet és a privát IP-címet külön előtér-IPs néven.</span><span class="sxs-lookup"><span data-stu-id="e4441-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="e4441-114">Példák</span><span class="sxs-lookup"><span data-stu-id="e4441-114">EXAMPLES</span></span>

### <span data-ttu-id="e4441-115">1. példa: nyilvános IP-cím hozzáadása előtér-IP-címhez</span><span class="sxs-lookup"><span data-stu-id="e4441-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="e4441-116">Az első parancs létrehozza a nyilvános IP-cím objektumot, és a $PublicIp változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="e4441-117">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e4441-118">A harmadik parancs hozzáadja a FrontEndIp01 nevű előtér-IP-konfigurációt a $AppGw átjáróhoz az $PublicIp tárolt címmel.</span><span class="sxs-lookup"><span data-stu-id="e4441-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="e4441-119">2. példa: statikus magánhálózati IP-cím hozzáadása előtér-IP-címhez</span><span class="sxs-lookup"><span data-stu-id="e4441-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="e4441-120">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e4441-121">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e4441-122">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e4441-123">A negyedik parancs hozzáadja a FrontendIP02 nevű előtér-IP-konfigurációt $Subnet a második parancsból és a privát IP-cím 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="e4441-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="e4441-124">3. példa: dinamikus privát IP hozzáadása előtér-IP-címhez</span><span class="sxs-lookup"><span data-stu-id="e4441-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="e4441-125">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e4441-126">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e4441-127">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4441-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e4441-128">A negyedik parancs a második parancs segítségével felveszi a FrontendIP02 nevű előtér-IP-konfigurációt a $Subnet használatával.</span><span class="sxs-lookup"><span data-stu-id="e4441-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="e4441-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4441-129">PARAMETERS</span></span>

### <span data-ttu-id="e4441-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4441-130">-ApplicationGateway</span></span>
<span data-ttu-id="e4441-131">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag hozzáadja az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e4441-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e4441-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4441-132">-DefaultProfile</span></span>
<span data-ttu-id="e4441-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4441-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4441-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4441-134">-Name</span></span>
<span data-ttu-id="e4441-135">A hozzáadni kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4441-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="e4441-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="e4441-136">-PrivateIPAddress</span></span>
<span data-ttu-id="e4441-137">Annak a magánhálózati IP-címnek a megadása, amelyet előtérként szeretne hozzáadni az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e4441-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="e4441-138">Ha meg van adva, az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="e4441-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="e4441-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="e4441-139">-PublicIPAddress</span></span>
<span data-ttu-id="e4441-140">Annak a nyilvános IP-címnek a meghatározása, amelyet a parancsmag az alkalmazás-átjáró előtér-IP-címének ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="e4441-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="e4441-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="e4441-141">-PublicIPAddressId</span></span>
<span data-ttu-id="e4441-142">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amelyet a parancsmag az alkalmazás-átjáró előtér-IP-címének ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="e4441-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="e4441-143">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="e4441-143">-Subnet</span></span>
<span data-ttu-id="e4441-144">Azt az alhálózatot adja meg, amelyet a parancsmag az előtér IP-konfigurációként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="e4441-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="e4441-145">Ha ezt a paramétert adja meg, az azt jelenti, hogy az Application Gateway támogatja a privát IP-alapú konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e4441-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="e4441-146">Ha a *PrivateIPAddress* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="e4441-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="e4441-147">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e4441-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e4441-148">– NetI</span><span class="sxs-lookup"><span data-stu-id="e4441-148">-SubnetId</span></span>
<span data-ttu-id="e4441-149">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyet a parancsmag az előtér IP-konfigurációként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="e4441-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="e4441-150">A tompított alhálózat a privát IP-címet jelenti.</span><span class="sxs-lookup"><span data-stu-id="e4441-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="e4441-151">Ha a *PrivateIPAddresss* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="e4441-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="e4441-152">Egyéb esetben az egyik IP-címet az alhálózatról dinamikusan felveszi az alkalmazás-átjáró eleje.</span><span class="sxs-lookup"><span data-stu-id="e4441-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="e4441-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4441-153">CommonParameters</span></span>
<span data-ttu-id="e4441-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4441-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4441-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4441-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4441-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4441-156">INPUTS</span></span>

### <span data-ttu-id="e4441-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e4441-157">System.String</span></span>

## <span data-ttu-id="e4441-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4441-158">OUTPUTS</span></span>

### <span data-ttu-id="e4441-159">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4441-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4441-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4441-160">NOTES</span></span>

## <span data-ttu-id="e4441-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4441-161">RELATED LINKS</span></span>

[<span data-ttu-id="e4441-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e4441-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e4441-163">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e4441-163">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e4441-164">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e4441-164">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e4441-165">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e4441-165">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


