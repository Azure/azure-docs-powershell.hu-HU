---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4499daa24230b9ec0b4731aa7be17c6f040db7d6
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93680914"
---
# <span data-ttu-id="e9c32-101">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9c32-101">New-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e9c32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9c32-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c32-103">Hálózati kapcsolat IP-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e9c32-103">Creates a network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9c32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9c32-104">SYNTAX</span></span>

### <span data-ttu-id="e9c32-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9c32-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9c32-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c32-106">SetByResourceId</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9c32-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9c32-107">DESCRIPTION</span></span>
<span data-ttu-id="e9c32-108">A **New-AzureRmNetworkInterfaceIpConfig** parancsmag az Azure hálózati felület IP-konfigurációját hozza létre egy hálózati csatolóhoz.</span><span class="sxs-lookup"><span data-stu-id="e9c32-108">The **New-AzureRmNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="e9c32-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e9c32-109">EXAMPLES</span></span>

### <span data-ttu-id="e9c32-110">1: IP-konfiguráció létrehozása hálózati kapcsolat nyilvános IP-címével</span><span class="sxs-lookup"><span data-stu-id="e9c32-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzureRmPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzureRmNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="e9c32-111">Az első két parancs a myvnet nevű virtuális hálózatot és a korábban létrehozott mysubnet nevű alhálózatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="e9c32-112">Ezek a $vnet és a $Subnet-ban vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="e9c32-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="e9c32-113">A harmadik parancs egy korábban létrehozott nyilvános IP-címet kap a PIP1 nevű webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="e9c32-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="e9c32-114">A Forth parancs új IP-konfigurációt hoz létre az "IPConfig-1" néven az elsődleges IP-konfigurációnak, amelyben egy nyilvános IP-cím van társítva.</span><span class="sxs-lookup"><span data-stu-id="e9c32-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="e9c32-115">Az utolsó parancs ekkor létrehoz egy mynic1 nevű hálózati felületet az IP-konfiguráció használatával.</span><span class="sxs-lookup"><span data-stu-id="e9c32-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="e9c32-116">2: IP-konfiguráció létrehozása privát IP-címmel</span><span class="sxs-lookup"><span data-stu-id="e9c32-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzureRmNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzureRmNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="e9c32-117">Az első két parancs a myvnet nevű virtuális hálózatot és a korábban létrehozott mysubnet nevű alhálózatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="e9c32-118">Ezek a $vnet és a $Subnet-ban vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="e9c32-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="e9c32-119">A harmadik parancs az "IPConfig-2" nevű új IP-konfigurációt hoz létre privát IP-10.0.0.5 társítva.</span><span class="sxs-lookup"><span data-stu-id="e9c32-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="e9c32-120">Az utolsó parancs ekkor létrehoz egy mynic1 nevű hálózati felületet az IP-konfiguráció használatával.</span><span class="sxs-lookup"><span data-stu-id="e9c32-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="e9c32-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9c32-121">PARAMETERS</span></span>

### <span data-ttu-id="e9c32-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e9c32-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="e9c32-123">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e9c32-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="e9c32-125">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e9c32-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="e9c32-127">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e9c32-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="e9c32-129">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c32-130">-DefaultProfile</span></span>
<span data-ttu-id="e9c32-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9c32-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9c32-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e9c32-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="e9c32-133">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e9c32-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="e9c32-135">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e9c32-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="e9c32-137">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IPConfiguration tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="e9c32-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="e9c32-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="e9c32-139">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9c32-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e9c32-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9c32-140">-Name</span></span>
<span data-ttu-id="e9c32-141">A hálózati kapcsolat IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="e9c32-142">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="e9c32-142">-Primary</span></span>
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

### <span data-ttu-id="e9c32-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9c32-143">-PrivateIpAddress</span></span>
<span data-ttu-id="e9c32-144">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="e9c32-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e9c32-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="e9c32-146">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="e9c32-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e9c32-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9c32-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="e9c32-148">IPv4</span></span>
- <span data-ttu-id="e9c32-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="e9c32-149">IPv6</span></span>

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

### <span data-ttu-id="e9c32-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9c32-150">-PublicIpAddress</span></span>
<span data-ttu-id="e9c32-151">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="e9c32-152">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="e9c32-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="e9c32-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e9c32-153">-PublicIpAddressId</span></span>
<span data-ttu-id="e9c32-154">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="e9c32-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="e9c32-155">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="e9c32-155">-Subnet</span></span>
<span data-ttu-id="e9c32-156">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e9c32-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="e9c32-157">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="e9c32-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="e9c32-158">– NetI</span><span class="sxs-lookup"><span data-stu-id="e9c32-158">-SubnetId</span></span>
<span data-ttu-id="e9c32-159">Annak az alhálózatnak a hivatkozását adja meg, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="e9c32-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="e9c32-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c32-160">CommonParameters</span></span>
<span data-ttu-id="e9c32-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9c32-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c32-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c32-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c32-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9c32-163">INPUTS</span></span>

### <span data-ttu-id="e9c32-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9c32-164">None</span></span>
<span data-ttu-id="e9c32-165">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e9c32-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9c32-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9c32-166">OUTPUTS</span></span>

### <span data-ttu-id="e9c32-167">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9c32-167">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="e9c32-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9c32-168">NOTES</span></span>
* <span data-ttu-id="e9c32-169">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="e9c32-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e9c32-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9c32-170">RELATED LINKS</span></span>

[<span data-ttu-id="e9c32-171">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9c32-171">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e9c32-172">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9c32-172">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e9c32-173">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9c32-173">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e9c32-174">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9c32-174">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


