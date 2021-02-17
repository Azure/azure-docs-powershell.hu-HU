---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206854"
---
# <span data-ttu-id="0ee4a-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4a-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0ee4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ee4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee4a-103">Előlapi IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="0ee4a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ee4a-104">SYNTAX</span></span>

### <span data-ttu-id="0ee4a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ee4a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ee4a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0ee4a-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ee4a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ee4a-107">DESCRIPTION</span></span>
<span data-ttu-id="0ee4a-108">A **New-AzApplicationGatewayFrontendIPConfig** parancsmag előtér-IP-konfigurációt hoz létre egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="0ee4a-109">Az alkalmazás-átjárók kétféle előlapi IP-konfigurációt támogatnak:</span><span class="sxs-lookup"><span data-stu-id="0ee4a-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="0ee4a-110">Nyilvános IP-címek – Privát IP-címek belső terheléselosztás használatával.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="0ee4a-111">Az alkalmazás-átjáróknak legalább egy nyilvános IP-címük és egy személyes IP-címük lehet.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="0ee4a-112">A nyilvános IP-címet és a privát IP-címet külön kell hozzáadni előlapi IP-címként.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="0ee4a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ee4a-113">EXAMPLES</span></span>

### <span data-ttu-id="0ee4a-114">1. példa: Előlapi IP-konfiguráció létrehozása nyilvános IP-erőforrás-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="0ee4a-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="0ee4a-115">Az első parancs létrehoz egy nyilvános IP-erőforrásobjektumot, és azt a $PublicIP tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="0ee4a-116">A második parancs $PublicIP FrontEndIP01 nevű új előlapi IP-konfigurációt hoz létre, és a $FrontEnd tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="0ee4a-117">2. példa: Statikus privát IP létrehozása előlapi IP-címként</span><span class="sxs-lookup"><span data-stu-id="0ee4a-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="0ee4a-118">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="0ee4a-119">A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="0ee4a-120">A harmadik parancs létrehoz egy FrontEndIP02 nevű előlapi IP-konfigurációt a $Subnet használatával a második parancsból és a 10.0.1.1-es privát IP-címből, majd a $FrontEnd változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="0ee4a-121">3. példa: Dinamikus privát IP létrehozása előlapi IP-címként</span><span class="sxs-lookup"><span data-stu-id="0ee4a-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="0ee4a-122">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="0ee4a-123">A második parancs egy Alhálózat01 nevű alhálózati konfigurációt kap, $VNet az első parancsból, és a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="0ee4a-124">A harmadik parancs létrehoz egy FrontEndIP03 nevű előlapi IP-konfigurációt a második $Subnet használatával, és azt a $FrontEnd változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="0ee4a-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ee4a-125">PARAMETERS</span></span>

### <span data-ttu-id="0ee4a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee4a-126">-DefaultProfile</span></span>
<span data-ttu-id="0ee4a-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ee4a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0ee4a-128">-Name</span></span>
<span data-ttu-id="0ee4a-129">A parancsmag által létrehozott előlapi IP-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0ee4a-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ee4a-130">-PrivateIPAddress</span></span>
<span data-ttu-id="0ee4a-131">Azt a privát IP-címet adja meg, amelyet a parancsmag az alkalmazás átjárója előlapi IP-címével társít.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="0ee4a-132">Ezt csak alhálózat megadva esetén lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="0ee4a-133">Ez az IP-cím statikusan ki van osztva az alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="0ee4a-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ee4a-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="0ee4a-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ee4a-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="0ee4a-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0ee4a-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="0ee4a-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0ee4a-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="0ee4a-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ee4a-138">-PublicIPAddress</span></span>
<span data-ttu-id="0ee4a-139">Azt a nyilvános IP-címobjektumot adja meg, amelyet ez a parancsmag társít az alkalmazás átjárója előlapi IP-címével.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="0ee4a-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="0ee4a-140">-PublicIPAddressId</span></span>
<span data-ttu-id="0ee4a-141">Megadja azt a nyilvános IP-címazonosítót, amelyet ez a parancsmag társít az alkalmazás átjárójának előlapi IP-címével.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="0ee4a-142">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="0ee4a-142">-Subnet</span></span>
<span data-ttu-id="0ee4a-143">Azt az alhálózati objektumot adja meg, amelyet ez a parancsmag társít az alkalmazás átjárója előtér-IP-címével.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="0ee4a-144">Ha ezt a paramétert adja meg, az azt jelenti, hogy az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="0ee4a-145">Ha a *PrivateIPAddress* paraméter meg van adva, annak a paraméterben megadott alhálózathoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="0ee4a-146">Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="0ee4a-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0ee4a-147">-SubnetId</span></span>
<span data-ttu-id="0ee4a-148">Megadja azt az alhálózati azonosítót, amelyet ez a parancsmag társít az alkalmazás átjárójának előtér-IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="0ee4a-149">Ha megadja az *Alhálózat* paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="0ee4a-150">Ha a *PrivateIPAddress* paraméter meg van adva, annak az alhálózat által megadott *alhálózathoz kell tartozni.*</span><span class="sxs-lookup"><span data-stu-id="0ee4a-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="0ee4a-151">Ha *a PrivateIPAddress* nincs megadva, az alhálózat egyik IP-címe dinamikusan az alkalmazás-átjáró előtér-IP-címeként lesz felvéve.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="0ee4a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee4a-152">CommonParameters</span></span>
<span data-ttu-id="0ee4a-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee4a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee4a-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ee4a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee4a-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ee4a-155">INPUTS</span></span>

### <span data-ttu-id="0ee4a-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ee4a-156">None</span></span>

## <span data-ttu-id="0ee4a-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ee4a-157">OUTPUTS</span></span>

### <span data-ttu-id="0ee4a-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ee4a-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="0ee4a-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ee4a-159">NOTES</span></span>

## <span data-ttu-id="0ee4a-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ee4a-160">RELATED LINKS</span></span>

[<span data-ttu-id="0ee4a-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4a-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0ee4a-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4a-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0ee4a-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4a-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0ee4a-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4a-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


