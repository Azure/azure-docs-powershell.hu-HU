---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328548"
---
# <span data-ttu-id="131a5-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="131a5-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="131a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="131a5-102">SYNOPSIS</span></span>
<span data-ttu-id="131a5-103">Módosítja az előlapi IP-címek konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="131a5-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="131a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="131a5-104">SYNTAX</span></span>

### <span data-ttu-id="131a5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="131a5-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="131a5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="131a5-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="131a5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="131a5-107">DESCRIPTION</span></span>
<span data-ttu-id="131a5-108">A **Set-AzApplicationGatewayFrontendIPConfig** parancsmag frissíti az előtér-IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="131a5-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="131a5-109">Az alkalmazás-átjárók kétféle előlapi IP-címet támogatnak:</span><span class="sxs-lookup"><span data-stu-id="131a5-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="131a5-110">Nyilvános IP-címek</span><span class="sxs-lookup"><span data-stu-id="131a5-110">Public IP addresses</span></span>
- <span data-ttu-id="131a5-111">Azok a privát IP-címek, amelyekhez a konfiguráció belső terheléselosztást (ILB) használ, az alkalmazás-átjáróknak legalább egy nyilvános IP-címük és egy személyes IP-címük lehet.</span><span class="sxs-lookup"><span data-stu-id="131a5-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="131a5-112">A nyilvános IP-címet és a személyes IP-címet külön kell hozzáadni előlapi IP-címként.</span><span class="sxs-lookup"><span data-stu-id="131a5-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="131a5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="131a5-113">EXAMPLES</span></span>

### <span data-ttu-id="131a5-114">1. példa: Nyilvános IP beállítása egy alkalmazásátjáró előlapi IP-címeként</span><span class="sxs-lookup"><span data-stu-id="131a5-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="131a5-115">Az első parancs létrehoz egy nyilvános IP-címobjektumot, és azt a $PublicIp tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="131a5-116">A második parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="131a5-117">A harmadik parancs frissíti a FrontEndIp01 nevű előlapi IP-konfigurációt az $AppGw-beli átjáróhoz a $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="131a5-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="131a5-118">2. példa: Statikus privát IP beállítása egy alkalmazásátjáró előlapi IP-címeként</span><span class="sxs-lookup"><span data-stu-id="131a5-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="131a5-119">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="131a5-120">A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="131a5-121">A harmadik parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="131a5-122">A negyedik parancs hozzáad egy FrontendIP02 nevű előlapi IP-konfigurációt a második parancs $Subnet és a 10.0.1.1-es privát IP-cím használatával.</span><span class="sxs-lookup"><span data-stu-id="131a5-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="131a5-123">3. példa: Dinamikus privát IP beállítása egy alkalmazásátjáró előlapi IP-címeként</span><span class="sxs-lookup"><span data-stu-id="131a5-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="131a5-124">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="131a5-125">A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="131a5-126">A harmadik parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="131a5-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="131a5-127">A negyedik parancs hozzáad egy FrontendIP02 nevű előlapi IP-konfigurációt a $Subnet parancsból származó adatok használatával.</span><span class="sxs-lookup"><span data-stu-id="131a5-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="131a5-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="131a5-128">PARAMETERS</span></span>

### <span data-ttu-id="131a5-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="131a5-129">-ApplicationGateway</span></span>
<span data-ttu-id="131a5-130">Egy olyan alkalmazás átjáróobjektumot ad meg, amelyben módosítani szeretné az előlapi IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="131a5-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="131a5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131a5-131">-DefaultProfile</span></span>
<span data-ttu-id="131a5-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="131a5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="131a5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="131a5-133">-Name</span></span>
<span data-ttu-id="131a5-134">A parancsmag által módosított előlapi IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="131a5-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="131a5-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="131a5-135">-PrivateIPAddress</span></span>
<span data-ttu-id="131a5-136">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="131a5-136">Specifies the private IP address.</span></span>
<span data-ttu-id="131a5-137">Ha meg van adva, az IP-cím statikusan ki van osztva az alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="131a5-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="131a5-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="131a5-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="131a5-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="131a5-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="131a5-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="131a5-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="131a5-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="131a5-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="131a5-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="131a5-142">-PublicIPAddress</span></span>
<span data-ttu-id="131a5-143">A nyilvános IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="131a5-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="131a5-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="131a5-144">-PublicIPAddressId</span></span>
<span data-ttu-id="131a5-145">A nyilvános IP-cím azonosítója.</span><span class="sxs-lookup"><span data-stu-id="131a5-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="131a5-146">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="131a5-146">-Subnet</span></span>
<span data-ttu-id="131a5-147">Az alkalmazás átjáró által használt alhálózata.</span><span class="sxs-lookup"><span data-stu-id="131a5-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="131a5-148">Akkor adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="131a5-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="131a5-149">Ha a *PrivateIPAddress* cím meg van adva, annak ehhez az alhálózathoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="131a5-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="131a5-150">Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.</span><span class="sxs-lookup"><span data-stu-id="131a5-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="131a5-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="131a5-151">-SubnetId</span></span>
<span data-ttu-id="131a5-152">Az alhálózat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="131a5-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="131a5-153">Akkor adja meg ezt a paramétert, ha az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="131a5-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="131a5-154">Ha a *PrivateIPAddress* paraméter meg van adva, annak ehhez az alhálózathoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="131a5-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="131a5-155">Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.</span><span class="sxs-lookup"><span data-stu-id="131a5-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="131a5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131a5-156">CommonParameters</span></span>
<span data-ttu-id="131a5-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131a5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131a5-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="131a5-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131a5-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="131a5-159">INPUTS</span></span>

### <span data-ttu-id="131a5-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="131a5-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="131a5-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="131a5-161">OUTPUTS</span></span>

### <span data-ttu-id="131a5-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="131a5-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="131a5-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="131a5-163">NOTES</span></span>

## <span data-ttu-id="131a5-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="131a5-164">RELATED LINKS</span></span>

[<span data-ttu-id="131a5-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="131a5-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="131a5-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="131a5-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="131a5-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="131a5-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="131a5-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="131a5-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="131a5-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="131a5-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


