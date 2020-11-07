---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 587ae151830f4d4860aa90c25b80a799e1ba2946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670699"
---
# <span data-ttu-id="6b718-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b718-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="6b718-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b718-102">SYNOPSIS</span></span>
<span data-ttu-id="6b718-103">Hálózati összeköttetés IP-konfigurációjának hozzáadása hálózati kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="6b718-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="6b718-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b718-104">SYNTAX</span></span>

### <span data-ttu-id="6b718-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b718-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b718-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b718-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b718-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b718-107">DESCRIPTION</span></span>
<span data-ttu-id="6b718-108">Az **Add-AzNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati interfészéhez illeszti be.</span><span class="sxs-lookup"><span data-stu-id="6b718-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="6b718-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6b718-109">EXAMPLES</span></span>

### <span data-ttu-id="6b718-110">1. példa: új IP-konfiguráció felvétele alkalmazás-biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="6b718-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="6b718-111">Ebben a példában olyan új hálózati illesztőfelület-MyNetworkInterface hozunk létre, amely az új virtuális hálózat MyVNET alhálózatához tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="6b718-112">Ezenkívül létrehozunk egy üres alkalmazások biztonsági csoportjának MyASG, amely a hálózati felületen az IP-konfigurációkkal társítható.</span><span class="sxs-lookup"><span data-stu-id="6b718-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="6b718-113">Miután mindkét objektumot létrehozta, az alapértelmezett IP-konfigurációt az MyASG objektumhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="6b718-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="6b718-114">Végül a hálózati felületen új IP-konfigurációt hozunk létre, amely az alkalmazás biztonsági csoport objektumához is csatolva van.</span><span class="sxs-lookup"><span data-stu-id="6b718-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="6b718-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b718-115">PARAMETERS</span></span>

### <span data-ttu-id="6b718-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b718-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="6b718-117">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b718-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="6b718-119">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b718-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="6b718-121">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6b718-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="6b718-123">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b718-124">-DefaultProfile</span></span>
<span data-ttu-id="6b718-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b718-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b718-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b718-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="6b718-127">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b718-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="6b718-129">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="6b718-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="6b718-131">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="6b718-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="6b718-133">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b718-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b718-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b718-134">-Name</span></span>
<span data-ttu-id="6b718-135">A hálózati kapcsolat IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b718-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b718-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b718-136">-NetworkInterface</span></span>
<span data-ttu-id="6b718-137">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b718-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="6b718-138">Ez a parancsmag a hálózati kapcsolat IP-konfigurációját hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="6b718-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b718-139">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="6b718-139">-Primary</span></span>
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

### <span data-ttu-id="6b718-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b718-140">-PrivateIpAddress</span></span>
<span data-ttu-id="6b718-141">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b718-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b718-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6b718-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="6b718-143">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b718-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="6b718-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6b718-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b718-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="6b718-145">IPv4</span></span>
- <span data-ttu-id="6b718-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="6b718-146">IPv6</span></span>

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

### <span data-ttu-id="6b718-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b718-147">-PublicIpAddress</span></span>
<span data-ttu-id="6b718-148">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b718-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="6b718-149">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="6b718-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b718-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6b718-150">-PublicIpAddressId</span></span>
<span data-ttu-id="6b718-151">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="6b718-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b718-152">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="6b718-152">-Subnet</span></span>
<span data-ttu-id="6b718-153">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b718-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="6b718-154">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="6b718-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="6b718-155">– NetI</span><span class="sxs-lookup"><span data-stu-id="6b718-155">-SubnetId</span></span>
<span data-ttu-id="6b718-156">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="6b718-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="6b718-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b718-157">CommonParameters</span></span>
<span data-ttu-id="6b718-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b718-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b718-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b718-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b718-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b718-160">INPUTS</span></span>

### <span data-ttu-id="6b718-161">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b718-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="6b718-162">System. string []</span><span class="sxs-lookup"><span data-stu-id="6b718-162">System.String[]</span></span>

### <span data-ttu-id="6b718-163">Microsoft. Azure. commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="6b718-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="6b718-164">Microsoft. Azure. commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="6b718-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="6b718-165">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="6b718-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="6b718-166">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="6b718-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="6b718-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b718-167">OUTPUTS</span></span>

### <span data-ttu-id="6b718-168">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b718-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6b718-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b718-169">NOTES</span></span>
* <span data-ttu-id="6b718-170">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="6b718-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6b718-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b718-171">RELATED LINKS</span></span>

[<span data-ttu-id="6b718-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b718-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6b718-173">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b718-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6b718-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b718-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6b718-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b718-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
