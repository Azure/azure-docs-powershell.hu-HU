---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353777"
---
# <span data-ttu-id="d0f53-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d0f53-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="d0f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f53-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f53-103">Előlapi IP-konfigurációt ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d0f53-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="d0f53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0f53-104">SYNTAX</span></span>

### <span data-ttu-id="d0f53-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f53-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f53-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d0f53-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f53-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0f53-107">DESCRIPTION</span></span>
<span data-ttu-id="d0f53-108">Az **Add-AzApplicationGatewayFrontendIPConfig** parancsmag előtér-IP-konfigurációt ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d0f53-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="d0f53-109">Az alkalmazásátjárók kétféle előlapi IP-konfigurációt támogatnak:</span><span class="sxs-lookup"><span data-stu-id="d0f53-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="d0f53-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="d0f53-110">Public IP addresses</span></span>
- <span data-ttu-id="d0f53-111">Privát IP-címek belső terheléselosztással (ILB) Az alkalmazás-átjáróknak legalább egy nyilvános IP-címük és egy privát IP-címük lehet.</span><span class="sxs-lookup"><span data-stu-id="d0f53-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="d0f53-112">Vegye fel a nyilvános IP-címet és a privát IP-címet külön előlapi IP-címként.</span><span class="sxs-lookup"><span data-stu-id="d0f53-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="d0f53-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0f53-113">EXAMPLES</span></span>

### <span data-ttu-id="d0f53-114">1. példa: Nyilvános IP-cím hozzáadása előlapi IP-címként</span><span class="sxs-lookup"><span data-stu-id="d0f53-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="d0f53-115">Az első parancs létrehoz egy nyilvános IP-címobjektumot, és azt a $PublicIp tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="d0f53-116">A második parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0f53-117">A harmadik parancs hozzáadja a FrontEndIp01 nevű előlapi IP-konfigurációt az $AppGw-beli átjáróhoz a $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="d0f53-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="d0f53-118">2. példa: Statikus privát IP-cím hozzáadása előlapi IP-címként</span><span class="sxs-lookup"><span data-stu-id="d0f53-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="d0f53-119">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="d0f53-120">A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="d0f53-121">A harmadik parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0f53-122">A negyedik parancs hozzáad egy FrontendIP02 nevű előlapi IP-konfigurációt a második parancs $Subnet és a 10.0.1.1-es privát IP-cím használatával.</span><span class="sxs-lookup"><span data-stu-id="d0f53-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="d0f53-123">3. példa: Dinamikus privát IP-cím hozzáadása előlapi IP-címként</span><span class="sxs-lookup"><span data-stu-id="d0f53-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="d0f53-124">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="d0f53-125">A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="d0f53-126">A harmadik parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0f53-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0f53-127">A negyedik parancs hozzáad egy FrontendIP02 nevű előlapi IP-konfigurációt a $Subnet parancsból származó adatok használatával.</span><span class="sxs-lookup"><span data-stu-id="d0f53-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="d0f53-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0f53-128">PARAMETERS</span></span>

### <span data-ttu-id="d0f53-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0f53-129">-ApplicationGateway</span></span>
<span data-ttu-id="d0f53-130">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag előlapi IP-konfigurációt ad.</span><span class="sxs-lookup"><span data-stu-id="d0f53-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d0f53-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f53-131">-DefaultProfile</span></span>
<span data-ttu-id="d0f53-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0f53-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0f53-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d0f53-133">-Name</span></span>
<span data-ttu-id="d0f53-134">Az előlapi IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0f53-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="d0f53-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="d0f53-135">-PrivateIPAddress</span></span>
<span data-ttu-id="d0f53-136">Megadja az alkalmazás átjárója előlapi IP-címeként hozzáadni szükséges személyes IP-címet.</span><span class="sxs-lookup"><span data-stu-id="d0f53-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="d0f53-137">Ha meg van adva, az IP-cím statikusan ki van osztva az alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="d0f53-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="d0f53-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f53-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="d0f53-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f53-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="d0f53-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0f53-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="d0f53-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0f53-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="d0f53-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="d0f53-142">-PublicIPAddress</span></span>
<span data-ttu-id="d0f53-143">Azt a nyilvános IP-címet adja meg, amelyet ez a parancsmag előlapi IP-címként ad hozzá az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d0f53-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="d0f53-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="d0f53-144">-PublicIPAddressId</span></span>
<span data-ttu-id="d0f53-145">Annak a nyilvános IP-címnek az azonosítója, amelyet ez a parancsmag előlapi IP-címként ad hozzá az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d0f53-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="d0f53-146">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="d0f53-146">-Subnet</span></span>
<span data-ttu-id="d0f53-147">Azt az alhálózatot adja meg, amelyet ez a parancsmag előtér-IP-konfigurációként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="d0f53-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="d0f53-148">Ha ezt a paramétert adja meg, az azt jelenti, hogy az alkalmazás átjárója támogatja a privát IP-alapú konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="d0f53-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="d0f53-149">Ha a *PrivateIPAddress* paraméter meg van adva, annak ehhez az alhálózathoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="d0f53-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="d0f53-150">Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.</span><span class="sxs-lookup"><span data-stu-id="d0f53-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d0f53-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d0f53-151">-SubnetId</span></span>
<span data-ttu-id="d0f53-152">Azt az alhálózati azonosítót adja meg, amelyet ez a parancsmag az előtér-IP-konfigurációként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="d0f53-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="d0f53-153">Az alhálózat átadása magánjellegű IP-címet jelent.</span><span class="sxs-lookup"><span data-stu-id="d0f53-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="d0f53-154">Ha a *PrivateIPAddress* paraméter meg van adva, annak ehhez az alhálózathoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="d0f53-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="d0f53-155">Ellenkező esetben az alhálózat egyik IP-címe dinamikusan az alkalmazás átjárója előtér-IP-címeként lesz felveve.</span><span class="sxs-lookup"><span data-stu-id="d0f53-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="d0f53-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f53-156">CommonParameters</span></span>
<span data-ttu-id="d0f53-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f53-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f53-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0f53-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f53-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0f53-159">INPUTS</span></span>

### <span data-ttu-id="d0f53-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0f53-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0f53-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0f53-161">OUTPUTS</span></span>

### <span data-ttu-id="d0f53-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0f53-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0f53-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0f53-163">NOTES</span></span>

## <span data-ttu-id="d0f53-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0f53-164">RELATED LINKS</span></span>

[<span data-ttu-id="d0f53-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d0f53-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d0f53-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d0f53-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d0f53-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d0f53-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d0f53-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d0f53-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


