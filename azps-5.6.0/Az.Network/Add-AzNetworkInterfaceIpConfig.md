---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 47ad7c00c2db310003dcc87b20405d05ec7f1f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009478"
---
# <span data-ttu-id="abcce-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="abcce-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="abcce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abcce-102">SYNOPSIS</span></span>
<span data-ttu-id="abcce-103">Hálózati felület IP-konfigurációjának hozzáadása hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="abcce-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="abcce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="abcce-104">SYNTAX</span></span>

### <span data-ttu-id="abcce-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abcce-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abcce-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="abcce-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abcce-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="abcce-107">DESCRIPTION</span></span>
<span data-ttu-id="abcce-108">Az **Add-AzNetworkInterfaceIpConfig** parancsmag hozzáadja a hálózati felületek IP-konfigurációját egy Azure hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="abcce-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="abcce-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="abcce-109">EXAMPLES</span></span>

### <span data-ttu-id="abcce-110">1. példa: Új IP-konfiguráció hozzáadása alkalmazásbiztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="abcce-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="abcce-111">Ebben a példában létrehozunk egy myNetworkInterface nevű új hálózati felületet, amely a MyVNET új virtuális hálózatának egy alhálózatához tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="abcce-112">Létrehozunk egy üres, MyASG alkalmazásbiztonsági csoportot is, amely a hálózati felületen az IP-konfigurációkat társítja.</span><span class="sxs-lookup"><span data-stu-id="abcce-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="abcce-113">Miután mindkét objektumot létrehozta, összekapcsoljuk az alapértelmezett IP-konfigurációt a MyASG objektummal.</span><span class="sxs-lookup"><span data-stu-id="abcce-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="abcce-114">Végül létrehozunk egy új IP-konfigurációt a hálózati felületen, amely az alkalmazás biztonsági csoportobjektumához is kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="abcce-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="abcce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abcce-115">PARAMETERS</span></span>

### <span data-ttu-id="abcce-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="abcce-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="abcce-117">Az alkalmazás-átjáró háttércímkészletének azon hivatkozásai gyűjteménye, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="abcce-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="abcce-119">Az alkalmazás-átjáró háttércímkészletének azon hivatkozásai gyűjteménye, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="abcce-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="abcce-121">Az alkalmazásbiztonsági csoport azon hivatkozásgyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="abcce-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="abcce-123">Az alkalmazásbiztonsági csoport azon hivatkozásgyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abcce-124">-DefaultProfile</span></span>
<span data-ttu-id="abcce-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abcce-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abcce-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="abcce-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="abcce-127">Azt a terheléselosztási háttércímkészlet-hivatkozásokat gyűjti össze, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="abcce-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="abcce-129">Azt a terheléselosztási háttércímkészlet-hivatkozásokat gyűjti össze, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="abcce-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="abcce-131">Azt a terheléselosztási bejövő hálózati címfordítási (NAT-) szabályhivatkozások gyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="abcce-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="abcce-133">Azt a terheléselosztási bejövő NAT-szabályhivatkozásokat gyűjti össze, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="abcce-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-134">-Name</span><span class="sxs-lookup"><span data-stu-id="abcce-134">-Name</span></span>
<span data-ttu-id="abcce-135">A hálózati felület IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcce-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="abcce-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="abcce-136">-NetworkInterface</span></span>
<span data-ttu-id="abcce-137">**NetworkInterface objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="abcce-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="abcce-138">Ez a parancsmag hozzáadja a hálózati felület IP-konfigurációját a paraméter által megadott objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="abcce-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="abcce-139">-Primary</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="abcce-140">-PrivateIpAddress</span></span>
<span data-ttu-id="abcce-141">A hálózati felület IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcce-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="abcce-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="abcce-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="abcce-143">Egy hálózatifelület-IP-konfiguráció IP-címének IP-verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcce-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="abcce-144">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="abcce-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abcce-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="abcce-145">IPv4</span></span>
- <span data-ttu-id="abcce-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="abcce-146">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcce-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="abcce-147">-PublicIpAddress</span></span>
<span data-ttu-id="abcce-148">Egy **PublicIPAddress objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="abcce-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="abcce-149">Ez a parancsmag egy nyilvános IP-címre hivatkozik, és ezzel a hálózati felület IP-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="abcce-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="abcce-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="abcce-150">-PublicIpAddressId</span></span>
<span data-ttu-id="abcce-151">Ez a parancsmag egy nyilvános IP-címre hivatkozik, és ezzel a hálózati felület IP-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="abcce-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="abcce-152">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="abcce-152">-Subnet</span></span>
<span data-ttu-id="abcce-153">**Alhálózati objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="abcce-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="abcce-154">Ez a parancsmag egy alhálózatra hivatkozik, amelyben létrejön a hálózati felület IP-konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="abcce-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="abcce-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="abcce-155">-SubnetId</span></span>
<span data-ttu-id="abcce-156">Ez a parancsmag egy alhálózatra hivatkozik, amelyben létrejön a hálózati felület IP-konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="abcce-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="abcce-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcce-157">CommonParameters</span></span>
<span data-ttu-id="abcce-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abcce-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcce-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcce-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcce-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abcce-160">INPUTS</span></span>

### <span data-ttu-id="abcce-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="abcce-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="abcce-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="abcce-162">System.String[]</span></span>

### <span data-ttu-id="abcce-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="abcce-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="abcce-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="abcce-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="abcce-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="abcce-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="abcce-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="abcce-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="abcce-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcce-167">OUTPUTS</span></span>

### <span data-ttu-id="abcce-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="abcce-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="abcce-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="abcce-169">NOTES</span></span>
* <span data-ttu-id="abcce-170">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="abcce-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="abcce-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abcce-171">RELATED LINKS</span></span>

[<span data-ttu-id="abcce-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="abcce-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="abcce-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="abcce-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="abcce-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="abcce-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="abcce-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="abcce-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
