---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0c244248a01038f6b22ec6037a1320df131d4b18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841809"
---
# <span data-ttu-id="76829-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76829-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="76829-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76829-102">SYNOPSIS</span></span>
<span data-ttu-id="76829-103">Hálózati összeköttetés IP-konfigurációjának hozzáadása hálózati kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="76829-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="76829-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76829-104">SYNTAX</span></span>

### <span data-ttu-id="76829-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76829-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76829-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="76829-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76829-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76829-107">DESCRIPTION</span></span>
<span data-ttu-id="76829-108">Az **Add-AzNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati interfészéhez illeszti be.</span><span class="sxs-lookup"><span data-stu-id="76829-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="76829-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76829-109">EXAMPLES</span></span>

### <span data-ttu-id="76829-110">1. példa: új IP-konfiguráció felvétele alkalmazás-biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="76829-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzNetworkInterface
```

<span data-ttu-id="76829-111">Ebben a példában olyan új hálózati illesztőfelület-MyNetworkInterface hozunk létre, amely az új virtuális hálózat MyVNET alhálózatához tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="76829-112">Ezenkívül létrehozunk egy üres alkalmazások biztonsági csoportjának MyASG, amely a hálózati felületen az IP-konfigurációkkal társítható.</span><span class="sxs-lookup"><span data-stu-id="76829-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="76829-113">Miután mindkét objektumot létrehozta, az alapértelmezett IP-konfigurációt az MyASG objektumhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="76829-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="76829-114">Végül a hálózati felületen új IP-konfigurációt hozunk létre, amely az alkalmazás biztonsági csoport objektumához is csatolva van.</span><span class="sxs-lookup"><span data-stu-id="76829-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="76829-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76829-115">PARAMETERS</span></span>

### <span data-ttu-id="76829-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76829-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="76829-117">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="76829-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="76829-119">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="76829-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="76829-121">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="76829-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="76829-123">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76829-124">-DefaultProfile</span></span>
<span data-ttu-id="76829-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76829-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76829-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76829-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="76829-127">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="76829-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="76829-129">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="76829-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="76829-131">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="76829-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="76829-133">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="76829-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76829-134">-Name</span></span>
<span data-ttu-id="76829-135">A hálózati kapcsolat IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76829-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="76829-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76829-136">-NetworkInterface</span></span>
<span data-ttu-id="76829-137">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="76829-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="76829-138">Ez a parancsmag a hálózati kapcsolat IP-konfigurációját hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="76829-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76829-139">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="76829-139">-Primary</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76829-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="76829-140">-PrivateIpAddress</span></span>
<span data-ttu-id="76829-141">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76829-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="76829-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="76829-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="76829-143">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="76829-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="76829-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76829-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76829-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="76829-145">IPv4</span></span>
- <span data-ttu-id="76829-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="76829-146">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76829-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="76829-147">-PublicIpAddress</span></span>
<span data-ttu-id="76829-148">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="76829-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="76829-149">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="76829-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="76829-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="76829-150">-PublicIpAddressId</span></span>
<span data-ttu-id="76829-151">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="76829-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="76829-152">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="76829-152">-Subnet</span></span>
<span data-ttu-id="76829-153">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="76829-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="76829-154">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="76829-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="76829-155">– NetI</span><span class="sxs-lookup"><span data-stu-id="76829-155">-SubnetId</span></span>
<span data-ttu-id="76829-156">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="76829-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="76829-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76829-157">CommonParameters</span></span>
<span data-ttu-id="76829-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76829-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76829-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76829-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76829-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76829-160">INPUTS</span></span>

### <span data-ttu-id="76829-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76829-161">PSNetworkInterface</span></span>
<span data-ttu-id="76829-162">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="76829-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="76829-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76829-163">OUTPUTS</span></span>

### <span data-ttu-id="76829-164">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76829-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="76829-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76829-165">NOTES</span></span>
* <span data-ttu-id="76829-166">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="76829-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="76829-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76829-167">RELATED LINKS</span></span>

[<span data-ttu-id="76829-168">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76829-168">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="76829-169">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76829-169">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="76829-170">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76829-170">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="76829-171">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76829-171">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


