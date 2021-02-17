---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156699"
---
# <span data-ttu-id="b16cd-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16cd-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="b16cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b16cd-103">Frissíti egy hálózati felület IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b16cd-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="b16cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b16cd-104">SYNTAX</span></span>

### <span data-ttu-id="b16cd-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b16cd-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b16cd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b16cd-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b16cd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b16cd-107">DESCRIPTION</span></span>
<span data-ttu-id="b16cd-108">A **Set-AzNetworkInterfaceIpConfig** parancsmag frissíti a hálózati felület IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b16cd-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="b16cd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b16cd-109">EXAMPLES</span></span>

### <span data-ttu-id="b16cd-110">1: IP-konfiguráció IP-címének módosítása</span><span class="sxs-lookup"><span data-stu-id="b16cd-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b16cd-111">Az első két parancs egy myvnet nevű virtuális hálózatot és egy mysubnet nevű alhálózatot kap, és tárolja a $vnet, illetve $subnet változókban.</span><span class="sxs-lookup"><span data-stu-id="b16cd-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="b16cd-112">A harmadik parancs a frissítandó IP-konfigurációhoz tartozó hálózati felületet (nic1) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b16cd-113">A harmadik parancs 10.0.0.11-re állítja az elsődleges IP-konfiguráció ipconfig1 ipconfig1-ét.</span><span class="sxs-lookup"><span data-stu-id="b16cd-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="b16cd-114">Végül az utolsó parancs frissíti a hálózati felületet, hogy a módosítások sikeresek legyenek.</span><span class="sxs-lookup"><span data-stu-id="b16cd-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="b16cd-115">2: IP-konfiguráció társítása alkalmazásbiztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="b16cd-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b16cd-116">Ebben a példában a $asg egy alkalmazásbiztonsági csoportra való hivatkozást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b16cd-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="b16cd-117">A negyedik parancs a frissítandó IP-konfigurációhoz tartozó hálózati felületet (nic1) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b16cd-118">A Set-AzNetworkInterfaceIpConfig ipconfig1 elsődleges IP-konfigurációjának privát IP-címét 10.0.0.11-re állítja, és létrehoz egy társítást a lekért alkalmazás biztonsági csoporttal.</span><span class="sxs-lookup"><span data-stu-id="b16cd-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="b16cd-119">Végül az utolsó parancs frissíti a hálózati felületet, hogy a módosítások sikeresek legyenek.</span><span class="sxs-lookup"><span data-stu-id="b16cd-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="b16cd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b16cd-120">PARAMETERS</span></span>

### <span data-ttu-id="b16cd-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16cd-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b16cd-122">Az alkalmazás-átjáró háttércímkészletének azon hivatkozásai gyűjteménye, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b16cd-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b16cd-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b16cd-124">Az alkalmazás-átjáró háttércímkészletének azon hivatkozásai gyűjteménye, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b16cd-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b16cd-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b16cd-126">Az alkalmazásbiztonsági csoportok azon hivatkozásgyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b16cd-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b16cd-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b16cd-128">Az alkalmazásbiztonsági csoport azon hivatkozásgyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b16cd-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16cd-129">-DefaultProfile</span></span>
<span data-ttu-id="b16cd-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b16cd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b16cd-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16cd-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b16cd-132">A hálózatifelület-IP-konfigurációhoz tartozó terheléselosztási háttércímkészlet-hivatkozások gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="b16cd-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b16cd-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b16cd-134">A hálózatifelület-IP-konfigurációhoz tartozó terheléselosztási háttércímkészlet-hivatkozások gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="b16cd-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b16cd-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b16cd-136">Azt a terheléselosztási bejövő hálózati címfordítási (NAT-) szabályhivatkozást adja meg, amelyhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b16cd-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="b16cd-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b16cd-138">Azt a terheléselosztási bejövő NAT-szabályhivatkozásokat gyűjti össze, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b16cd-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b16cd-139">-Name</span><span class="sxs-lookup"><span data-stu-id="b16cd-139">-Name</span></span>
<span data-ttu-id="b16cd-140">Annak a hálózati IP-konfigurációnak a neve, amelyhez ez a parancsmag be van állítja.</span><span class="sxs-lookup"><span data-stu-id="b16cd-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="b16cd-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b16cd-141">-NetworkInterface</span></span>
<span data-ttu-id="b16cd-142">**NetworkInterface objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="b16cd-143">Ez a parancsmag hozzáadja a hálózati felület IP-konfigurációját a paraméter által megadott objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b16cd-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b16cd-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="b16cd-144">-Primary</span></span>
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

### <span data-ttu-id="b16cd-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b16cd-145">-PrivateIpAddress</span></span>
<span data-ttu-id="b16cd-146">A hálózati felület IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="b16cd-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b16cd-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b16cd-148">Egy hálózatifelület-IP-konfiguráció IP-címének IP-verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="b16cd-149">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b16cd-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b16cd-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="b16cd-150">IPv4</span></span>
- <span data-ttu-id="b16cd-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="b16cd-151">IPv6</span></span>

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

### <span data-ttu-id="b16cd-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b16cd-152">-PublicIpAddress</span></span>
<span data-ttu-id="b16cd-153">Egy **PublicIPAddress objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="b16cd-154">Ez a parancsmag egy nyilvános IP-címre hivatkozik, és ezzel a hálózati felület IP-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="b16cd-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b16cd-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b16cd-155">-PublicIpAddressId</span></span>
<span data-ttu-id="b16cd-156">Ez a parancsmag egy nyilvános IP-címre hivatkozik, és ezzel a hálózati felület IP-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="b16cd-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b16cd-157">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="b16cd-157">-Subnet</span></span>
<span data-ttu-id="b16cd-158">**Alhálózati objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b16cd-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b16cd-159">Ez a parancsmag egy alhálózatra hivatkozik, amelyben létrejön a hálózati felület IP-konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="b16cd-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b16cd-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b16cd-160">-SubnetId</span></span>
<span data-ttu-id="b16cd-161">Ez a parancsmag egy alhálózatra hivatkozik, amelyben létrejön a hálózati felület IP-konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="b16cd-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b16cd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16cd-162">CommonParameters</span></span>
<span data-ttu-id="b16cd-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16cd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16cd-164">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b16cd-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16cd-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b16cd-165">INPUTS</span></span>

### <span data-ttu-id="b16cd-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b16cd-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="b16cd-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b16cd-167">System.String[]</span></span>

### <span data-ttu-id="b16cd-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="b16cd-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="b16cd-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="b16cd-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="b16cd-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="b16cd-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="b16cd-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="b16cd-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="b16cd-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b16cd-172">OUTPUTS</span></span>

### <span data-ttu-id="b16cd-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b16cd-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b16cd-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b16cd-174">NOTES</span></span>
* <span data-ttu-id="b16cd-175">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="b16cd-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b16cd-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b16cd-176">RELATED LINKS</span></span>

[<span data-ttu-id="b16cd-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16cd-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b16cd-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16cd-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b16cd-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16cd-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b16cd-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16cd-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
