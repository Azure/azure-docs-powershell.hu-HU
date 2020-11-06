---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 57c92345537e72a38c5228c0a10d38f6ad61d13a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504871"
---
# <span data-ttu-id="962f6-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="962f6-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="962f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="962f6-102">SYNOPSIS</span></span>
<span data-ttu-id="962f6-103">Hálózati összeköttetés IP-konfigurációjának hozzáadása hálózati kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="962f6-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="962f6-104">SYNTAX</span></span>

### <span data-ttu-id="962f6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="962f6-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="962f6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="962f6-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="962f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="962f6-107">DESCRIPTION</span></span>
<span data-ttu-id="962f6-108">Az **Add-AzureRmNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati interfészéhez illeszti be.</span><span class="sxs-lookup"><span data-stu-id="962f6-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="962f6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="962f6-109">EXAMPLES</span></span>

### <span data-ttu-id="962f6-110">1. példa: új IP-konfiguráció felvétele alkalmazás-biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="962f6-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="962f6-111">Ebben a példában olyan új hálózati illesztőfelület-MyNetworkInterface hozunk létre, amely az új virtuális hálózat MyVNET alhálózatához tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="962f6-112">Ezenkívül létrehozunk egy üres alkalmazások biztonsági csoportjának MyASG, amely a hálózati felületen az IP-konfigurációkkal társítható.</span><span class="sxs-lookup"><span data-stu-id="962f6-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="962f6-113">Miután mindkét objektumot létrehozta, az alapértelmezett IP-konfigurációt az MyASG objektumhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="962f6-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="962f6-114">Végül a hálózati felületen új IP-konfigurációt hozunk létre, amely az alkalmazás biztonsági csoport objektumához is csatolva van.</span><span class="sxs-lookup"><span data-stu-id="962f6-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="962f6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="962f6-115">PARAMETERS</span></span>

### <span data-ttu-id="962f6-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="962f6-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="962f6-117">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="962f6-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="962f6-119">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="962f6-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="962f6-121">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="962f6-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="962f6-123">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962f6-124">-DefaultProfile</span></span>
<span data-ttu-id="962f6-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="962f6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962f6-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="962f6-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="962f6-127">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="962f6-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="962f6-129">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="962f6-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="962f6-131">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="962f6-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="962f6-133">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="962f6-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="962f6-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="962f6-134">-Name</span></span>
<span data-ttu-id="962f6-135">A hálózati kapcsolat IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="962f6-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="962f6-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="962f6-136">-NetworkInterface</span></span>
<span data-ttu-id="962f6-137">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="962f6-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="962f6-138">Ez a parancsmag a hálózati kapcsolat IP-konfigurációját hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="962f6-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="962f6-139">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="962f6-139">-Primary</span></span>
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

### <span data-ttu-id="962f6-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="962f6-140">-PrivateIpAddress</span></span>
<span data-ttu-id="962f6-141">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="962f6-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="962f6-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="962f6-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="962f6-143">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="962f6-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="962f6-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="962f6-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="962f6-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="962f6-145">IPv4</span></span>
- <span data-ttu-id="962f6-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="962f6-146">IPv6</span></span>

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

### <span data-ttu-id="962f6-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="962f6-147">-PublicIpAddress</span></span>
<span data-ttu-id="962f6-148">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="962f6-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="962f6-149">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="962f6-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="962f6-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="962f6-150">-PublicIpAddressId</span></span>
<span data-ttu-id="962f6-151">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="962f6-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="962f6-152">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="962f6-152">-Subnet</span></span>
<span data-ttu-id="962f6-153">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="962f6-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="962f6-154">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="962f6-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="962f6-155">– NetI</span><span class="sxs-lookup"><span data-stu-id="962f6-155">-SubnetId</span></span>
<span data-ttu-id="962f6-156">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="962f6-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="962f6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962f6-157">CommonParameters</span></span>
<span data-ttu-id="962f6-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="962f6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962f6-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962f6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962f6-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="962f6-160">INPUTS</span></span>

### <span data-ttu-id="962f6-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="962f6-161">PSNetworkInterface</span></span>
<span data-ttu-id="962f6-162">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="962f6-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="962f6-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="962f6-163">OUTPUTS</span></span>

### <span data-ttu-id="962f6-164">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="962f6-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="962f6-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="962f6-165">NOTES</span></span>
* <span data-ttu-id="962f6-166">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="962f6-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="962f6-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="962f6-167">RELATED LINKS</span></span>

[<span data-ttu-id="962f6-168">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="962f6-168">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="962f6-169">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="962f6-169">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="962f6-170">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="962f6-170">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="962f6-171">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="962f6-171">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

