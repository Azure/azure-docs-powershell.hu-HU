---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1c48140b56e180f0002ef62c7d644535ac751546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496392"
---
# <span data-ttu-id="373e4-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="373e4-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="373e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="373e4-102">SYNOPSIS</span></span>
<span data-ttu-id="373e4-103">Előtér IP-konfigurációját hozza létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="373e4-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="373e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="373e4-104">SYNTAX</span></span>

### <span data-ttu-id="373e4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="373e4-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="373e4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="373e4-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="373e4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="373e4-107">DESCRIPTION</span></span>
<span data-ttu-id="373e4-108">A **New-AzureRmApplicationGatewayFrontendIPConfig** parancsmag létrehoz egy előtér IP-configuraton az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="373e4-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="373e4-109">Az alkalmazás-átjárók kétféle előtér-IP-konfigurációt támogatnak:</span><span class="sxs-lookup"><span data-stu-id="373e4-109">An application gateway supports two types of front-end IP configuration:</span></span> 

- <span data-ttu-id="373e4-110">Nyilvános IP-címek – privát IP-címek belső terheléselosztási (ILB) használatával.</span><span class="sxs-lookup"><span data-stu-id="373e4-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>

<span data-ttu-id="373e4-111">Az alkalmazás-átjárók legfeljebb egy nyilvános IP-címet és egy privát IP-címet tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="373e4-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="373e4-112">A nyilvános IP-címet és a privát IP-címet külön-külön kell hozzáadni az előtér-IP-címekhez.</span><span class="sxs-lookup"><span data-stu-id="373e4-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="373e4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="373e4-113">EXAMPLES</span></span>

### <span data-ttu-id="373e4-114">Példa 1: előtér IP-konfigurációjának létrehozása nyilvános IP-erőforrás-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="373e4-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="373e4-115">Az első parancs létrehoz egy nyilvános IP-erőforrás-objektumot, és a $PublicIP változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="373e4-116">A második parancs $PublicIP segítségével létrehoz egy FrontEndIP01 nevű új előtér-IP-konfigurációt, és a $FrontEnd változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="373e4-117">2. példa: statikus privát IP létrehozása előtér-IP-címként</span><span class="sxs-lookup"><span data-stu-id="373e4-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="373e4-118">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="373e4-119">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="373e4-120">A harmadik parancs létrehozza a $Subnet FrontEndIP02 nevű előtér-IP-konfigurációt a második parancs és a privát IP-cím 10.0.1.1, majd a $FrontEnd változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="373e4-121">3. példa: dinamikus privát IP-cím létrehozása előtér-IP-címként</span><span class="sxs-lookup"><span data-stu-id="373e4-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="373e4-122">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="373e4-123">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt az első parancs $VNet az első parancsból, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="373e4-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="373e4-124">A harmadik parancs a második parancs segítségével létrehoz egy FrontEndIP03 nevű előtér-IP-konfigurációt, és a $FrontEnd változóban tárolja a $Subnet.</span><span class="sxs-lookup"><span data-stu-id="373e4-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="373e4-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="373e4-125">PARAMETERS</span></span>

### <span data-ttu-id="373e4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373e4-126">-DefaultProfile</span></span>
<span data-ttu-id="373e4-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="373e4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="373e4-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="373e4-128">-Name</span></span>
<span data-ttu-id="373e4-129">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="373e4-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="373e4-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="373e4-130">-PrivateIPAddress</span></span>
<span data-ttu-id="373e4-131">Annak a magánhálózati IP-címnek a megadása, amelyhez ez a parancsmag társítva van az alkalmazás-átjáró előtér IP-címével.</span><span class="sxs-lookup"><span data-stu-id="373e4-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="373e4-132">Ez csak akkor adható meg, ha meg van adva alhálózat.</span><span class="sxs-lookup"><span data-stu-id="373e4-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="373e4-133">Az IP-cím statikusan van kiosztva az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="373e4-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="373e4-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="373e4-134">-PublicIPAddress</span></span>
<span data-ttu-id="373e4-135">Annak a nyilvános IP-cím objektumnak a meghatározása, amelyet ez a parancsmag társít az alkalmazás átjárójának előtér-IP-címéhez.</span><span class="sxs-lookup"><span data-stu-id="373e4-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="373e4-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="373e4-136">-PublicIPAddressId</span></span>
<span data-ttu-id="373e4-137">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amely a parancsmag a program átjárójának előtér-IP-címéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="373e4-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="373e4-138">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="373e4-138">-Subnet</span></span>
<span data-ttu-id="373e4-139">Annak az alhálózatnak az objektumát adja meg, amely a parancsmag a program átjárójának előtér-IP-címéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="373e4-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="373e4-140">Ha megadja ezt a paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="373e4-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="373e4-141">Ha a *PrivateIPAddresss* paramétert adja meg, akkor az a paraméter által meghatározott alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="373e4-141">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="373e4-142">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="373e4-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="373e4-143">– NetI</span><span class="sxs-lookup"><span data-stu-id="373e4-143">-SubnetId</span></span>
<span data-ttu-id="373e4-144">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag az alkalmazás-átjáró előtér-IP-konfigurációját társítja.</span><span class="sxs-lookup"><span data-stu-id="373e4-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="373e4-145">Ha megadja az *alhálózati* paramétert, az azt jelenti, hogy az átjáró privát IP-címet használ.</span><span class="sxs-lookup"><span data-stu-id="373e4-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="373e4-146">Ha a *PrivateIPAddress* paramétert adja meg, akkor az *alhálózat* által megadott alhálózathoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="373e4-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="373e4-147">Ha a *PrivateIPAddress* nincs megadva, az alhálózatból az egyik IP-címet dinamikusan felveszi az alkalmazás-átjáró előtér-IP-címe.</span><span class="sxs-lookup"><span data-stu-id="373e4-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="373e4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373e4-148">CommonParameters</span></span>
<span data-ttu-id="373e4-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="373e4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373e4-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373e4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373e4-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="373e4-151">INPUTS</span></span>

### <span data-ttu-id="373e4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="373e4-152">System.String</span></span>

## <span data-ttu-id="373e4-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="373e4-153">OUTPUTS</span></span>

### <span data-ttu-id="373e4-154">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="373e4-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="373e4-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="373e4-155">NOTES</span></span>

## <span data-ttu-id="373e4-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="373e4-156">RELATED LINKS</span></span>

[<span data-ttu-id="373e4-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="373e4-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="373e4-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="373e4-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="373e4-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="373e4-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="373e4-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="373e4-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


