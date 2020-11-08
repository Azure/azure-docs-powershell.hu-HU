---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183004"
---
# <span data-ttu-id="83965-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83965-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="83965-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83965-102">SYNOPSIS</span></span>
<span data-ttu-id="83965-103">Hálózati kapcsolat IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="83965-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="83965-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83965-104">SYNTAX</span></span>

### <span data-ttu-id="83965-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83965-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83965-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="83965-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83965-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83965-107">DESCRIPTION</span></span>
<span data-ttu-id="83965-108">A **New-AzNetworkInterfaceIpConfig** parancsmag az Azure hálózati felület IP-konfigurációját hozza létre egy hálózati csatolóhoz.</span><span class="sxs-lookup"><span data-stu-id="83965-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="83965-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83965-109">EXAMPLES</span></span>

### <span data-ttu-id="83965-110">1: IP-konfiguráció létrehozása hálózati kapcsolat nyilvános IP-címével</span><span class="sxs-lookup"><span data-stu-id="83965-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="83965-111">Az első két parancs a myvnet nevű virtuális hálózatot és a korábban létrehozott mysubnet nevű alhálózatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="83965-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="83965-112">Ezek a $vnet és a $Subnet-ban vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="83965-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="83965-113">A harmadik parancs egy korábban létrehozott nyilvános IP-címet kap a PIP1 nevű webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="83965-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="83965-114">A Forth parancs új IP-konfigurációt hoz létre az "IPConfig-1" néven az elsődleges IP-konfigurációnak, amelyben egy nyilvános IP-cím van társítva.</span><span class="sxs-lookup"><span data-stu-id="83965-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="83965-115">Az utolsó parancs ekkor létrehoz egy mynic1 nevű hálózati felületet az IP-konfiguráció használatával.</span><span class="sxs-lookup"><span data-stu-id="83965-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="83965-116">2: IP-konfiguráció létrehozása privát IP-címmel</span><span class="sxs-lookup"><span data-stu-id="83965-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="83965-117">Az első két parancs a myvnet nevű virtuális hálózatot és a korábban létrehozott mysubnet nevű alhálózatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="83965-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="83965-118">Ezek a $vnet és a $Subnet-ban vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="83965-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="83965-119">A harmadik parancs az "IPConfig-2" nevű új IP-konfigurációt hoz létre privát IP-10.0.0.5 társítva.</span><span class="sxs-lookup"><span data-stu-id="83965-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="83965-120">Az utolsó parancs ekkor létrehoz egy mynic1 nevű hálózati felületet az IP-konfiguráció használatával.</span><span class="sxs-lookup"><span data-stu-id="83965-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="83965-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83965-121">PARAMETERS</span></span>

### <span data-ttu-id="83965-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="83965-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="83965-123">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="83965-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="83965-125">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83965-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="83965-127">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="83965-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="83965-129">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83965-130">-DefaultProfile</span></span>
<span data-ttu-id="83965-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83965-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83965-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="83965-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="83965-133">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="83965-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="83965-135">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="83965-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="83965-137">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IPConfiguration tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="83965-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="83965-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="83965-139">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="83965-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="83965-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83965-140">-Name</span></span>
<span data-ttu-id="83965-141">A hálózati kapcsolat IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83965-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="83965-142">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="83965-142">-Primary</span></span>
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

### <span data-ttu-id="83965-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="83965-143">-PrivateIpAddress</span></span>
<span data-ttu-id="83965-144">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83965-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="83965-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="83965-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="83965-146">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="83965-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="83965-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="83965-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83965-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="83965-148">IPv4</span></span>
- <span data-ttu-id="83965-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="83965-149">IPv6</span></span>

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

### <span data-ttu-id="83965-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83965-150">-PublicIpAddress</span></span>
<span data-ttu-id="83965-151">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="83965-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="83965-152">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="83965-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="83965-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="83965-153">-PublicIpAddressId</span></span>
<span data-ttu-id="83965-154">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="83965-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="83965-155">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="83965-155">-Subnet</span></span>
<span data-ttu-id="83965-156">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="83965-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="83965-157">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="83965-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="83965-158">– NetI</span><span class="sxs-lookup"><span data-stu-id="83965-158">-SubnetId</span></span>
<span data-ttu-id="83965-159">Annak az alhálózatnak a hivatkozását adja meg, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="83965-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="83965-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83965-160">CommonParameters</span></span>
<span data-ttu-id="83965-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83965-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83965-162">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83965-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83965-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83965-163">INPUTS</span></span>

### <span data-ttu-id="83965-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="83965-164">System.String[]</span></span>

### <span data-ttu-id="83965-165">Microsoft. Azure. commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="83965-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="83965-166">Microsoft. Azure. commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="83965-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="83965-167">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="83965-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="83965-168">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="83965-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="83965-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83965-169">OUTPUTS</span></span>

### <span data-ttu-id="83965-170">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="83965-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="83965-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83965-171">NOTES</span></span>
* <span data-ttu-id="83965-172">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="83965-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="83965-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83965-173">RELATED LINKS</span></span>

[<span data-ttu-id="83965-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83965-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="83965-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83965-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="83965-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83965-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="83965-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83965-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
