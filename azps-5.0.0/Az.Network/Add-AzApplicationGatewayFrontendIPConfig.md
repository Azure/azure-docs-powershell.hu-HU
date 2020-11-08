---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187278"
---
# <span data-ttu-id="89067-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89067-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="89067-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89067-102">SYNOPSIS</span></span>
<span data-ttu-id="89067-103">Az előtér IP-konfigurációját hozzáadja egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="89067-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="89067-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89067-104">SYNTAX</span></span>

### <span data-ttu-id="89067-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="89067-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89067-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="89067-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89067-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="89067-107">DESCRIPTION</span></span>
<span data-ttu-id="89067-108">Az **Add-AzApplicationGatewayFrontendIPConfig** parancsmag egyoldalas IP-konfigurációt ad az alkalmazás-átjárónak.</span><span class="sxs-lookup"><span data-stu-id="89067-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="89067-109">Az alkalmazás-átjárók kétféle előtér-IP-konfigurációt támogatnak:</span><span class="sxs-lookup"><span data-stu-id="89067-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="89067-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="89067-110">Public IP addresses</span></span>
- <span data-ttu-id="89067-111">Privát IP-címek belső terheléselosztási (ILB) használatával az alkalmazás-átjárók legfeljebb egy nyilvános IP-címen és egy privát IP-címen lehetnek.</span><span class="sxs-lookup"><span data-stu-id="89067-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="89067-112">Adja meg a nyilvános IP-címet és a privát IP-címet külön előtér-IPs néven.</span><span class="sxs-lookup"><span data-stu-id="89067-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="89067-113">Példák</span><span class="sxs-lookup"><span data-stu-id="89067-113">EXAMPLES</span></span>

### <span data-ttu-id="89067-114">1. példa: nyilvános IP-cím hozzáadása előtér-IP-címhez</span><span class="sxs-lookup"><span data-stu-id="89067-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="89067-115">Az első parancs létrehozza a nyilvános IP-cím objektumot, és a $PublicIp változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="89067-116">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="89067-117">A harmadik parancs hozzáadja a FrontEndIp01 nevű előtér-IP-konfigurációt a $AppGw átjáróhoz az $PublicIp tárolt címmel.</span><span class="sxs-lookup"><span data-stu-id="89067-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="89067-118">2. példa: statikus magánhálózati IP-cím hozzáadása előtér-IP-címhez</span><span class="sxs-lookup"><span data-stu-id="89067-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="89067-119">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="89067-120">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="89067-121">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="89067-122">A negyedik parancs hozzáadja a FrontendIP02 nevű előtér-IP-konfigurációt $Subnet a második parancsból és a privát IP-cím 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="89067-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="89067-123">3. példa: dinamikus privát IP hozzáadása előtér-IP-címhez</span><span class="sxs-lookup"><span data-stu-id="89067-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="89067-124">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="89067-125">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="89067-126">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89067-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="89067-127">A negyedik parancs a második parancs segítségével felveszi a FrontendIP02 nevű előtér-IP-konfigurációt a $Subnet használatával.</span><span class="sxs-lookup"><span data-stu-id="89067-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="89067-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89067-128">PARAMETERS</span></span>

### <span data-ttu-id="89067-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89067-129">-ApplicationGateway</span></span>
<span data-ttu-id="89067-130">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag hozzáadja az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="89067-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="89067-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89067-131">-DefaultProfile</span></span>
<span data-ttu-id="89067-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89067-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89067-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89067-133">-Name</span></span>
<span data-ttu-id="89067-134">A hozzáadni kívánt előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89067-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="89067-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="89067-135">-PrivateIPAddress</span></span>
<span data-ttu-id="89067-136">Annak a magánhálózati IP-címnek a megadása, amelyet előtérként szeretne hozzáadni az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="89067-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="89067-137">Ha meg van adva, az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="89067-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="89067-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="89067-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="89067-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="89067-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="89067-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="89067-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="89067-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="89067-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="89067-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="89067-142">-PublicIPAddress</span></span>
<span data-ttu-id="89067-143">Annak a nyilvános IP-címnek a meghatározása, amelyet a parancsmag az alkalmazás-átjáró előtér-IP-címének ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="89067-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="89067-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="89067-144">-PublicIPAddressId</span></span>
<span data-ttu-id="89067-145">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amelyet a parancsmag az alkalmazás-átjáró előtér-IP-címének ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="89067-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="89067-146">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="89067-146">-Subnet</span></span>
<span data-ttu-id="89067-147">Azt az alhálózatot adja meg, amelyet a parancsmag az előtér IP-konfigurációként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="89067-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="89067-148">Ha ezt a paramétert adja meg, az azt jelenti, hogy az Application Gateway támogatja a privát IP-alapú konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="89067-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="89067-149">Ha a *PrivateIPAddress* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="89067-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="89067-150">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="89067-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="89067-151">– NetI</span><span class="sxs-lookup"><span data-stu-id="89067-151">-SubnetId</span></span>
<span data-ttu-id="89067-152">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyet a parancsmag az előtér IP-konfigurációként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="89067-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="89067-153">A tompított alhálózat a privát IP-címet jelenti.</span><span class="sxs-lookup"><span data-stu-id="89067-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="89067-154">Ha a *PrivateIPAddress* paramétert adja meg, akkor az az alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="89067-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="89067-155">Egyéb esetben az egyik IP-címet az alhálózatról dinamikusan felveszi az alkalmazás-átjáró eleje.</span><span class="sxs-lookup"><span data-stu-id="89067-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="89067-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89067-156">CommonParameters</span></span>
<span data-ttu-id="89067-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89067-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89067-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89067-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89067-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89067-159">INPUTS</span></span>

### <span data-ttu-id="89067-160">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89067-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89067-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89067-161">OUTPUTS</span></span>

### <span data-ttu-id="89067-162">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89067-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89067-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89067-163">NOTES</span></span>

## <span data-ttu-id="89067-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89067-164">RELATED LINKS</span></span>

[<span data-ttu-id="89067-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89067-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="89067-166">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89067-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="89067-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89067-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="89067-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89067-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

