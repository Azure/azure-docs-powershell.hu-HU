---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202794"
---
# <span data-ttu-id="1d318-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d318-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="1d318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d318-102">SYNOPSIS</span></span>
<span data-ttu-id="1d318-103">Hálózatifelület-IP-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1d318-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="1d318-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d318-104">SYNTAX</span></span>

### <span data-ttu-id="1d318-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d318-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d318-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d318-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d318-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d318-107">DESCRIPTION</span></span>
<span data-ttu-id="1d318-108">A **New-AzNetworkInterfaceIpConfig** parancsmag létrehoz egy Azure network interface IP-konfigurációt egy hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="1d318-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="1d318-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d318-109">EXAMPLES</span></span>

### <span data-ttu-id="1d318-110">1: IP-konfiguráció létrehozása nyilvános IP-címmel hálózati felülethez</span><span class="sxs-lookup"><span data-stu-id="1d318-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="1d318-111">Az első két parancs egy myvnet nevű virtuális hálózatot, illetve egy korábban létrehozott mysubnet nevű alhálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="1d318-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="1d318-112">Ezeket a fájlok a $vnet, illetve $Subnet tárolják.</span><span class="sxs-lookup"><span data-stu-id="1d318-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="1d318-113">A harmadik parancs egy korábban létrehozott, PIP1 nevű nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="1d318-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="1d318-114">A oda-vissza parancs létrehoz egy új IP-konfigurációt (IPConfig-1) elsődleges IP-konfigurációként, amely nyilvános IP-címmel van társítva.</span><span class="sxs-lookup"><span data-stu-id="1d318-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="1d318-115">Az utolsó parancs ezután létrehoz egy mynic1 nevű hálózati felületet ezzel az IP-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="1d318-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="1d318-116">2: IP-konfiguráció létrehozása privát IP-címmel</span><span class="sxs-lookup"><span data-stu-id="1d318-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="1d318-117">Az első két parancs egy myvnet nevű virtuális hálózatot, illetve egy korábban létrehozott mysubnet nevű alhálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="1d318-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="1d318-118">Ezeket a fájlok a $vnet, illetve $Subnet tárolják.</span><span class="sxs-lookup"><span data-stu-id="1d318-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="1d318-119">A harmadik parancs létrehoz egy új IP-konfigurációt (IPConfig-2) egy 10.0.0.5-ös személyes IP-címmel, amely hozzá van társítva.</span><span class="sxs-lookup"><span data-stu-id="1d318-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="1d318-120">Az utolsó parancs ezután létrehoz egy mynic1 nevű hálózati felületet ezzel az IP-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="1d318-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="1d318-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d318-121">PARAMETERS</span></span>

### <span data-ttu-id="1d318-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1d318-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="1d318-123">Az alkalmazás-átjáró háttércímkészletének azon hivatkozásai gyűjteménye, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1d318-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="1d318-125">Az alkalmazás-átjáró háttércímkészletének azon hivatkozásai gyűjteménye, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d318-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="1d318-127">Az alkalmazásbiztonsági csoport azon hivatkozásgyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1d318-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="1d318-129">Az alkalmazásbiztonsági csoport azon hivatkozásgyűjteményét adja meg, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d318-130">-DefaultProfile</span></span>
<span data-ttu-id="1d318-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d318-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d318-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1d318-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="1d318-133">Azt a terheléselosztási háttércímkészlet-hivatkozásokat gyűjti össze, amelyekhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1d318-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="1d318-135">A hálózatifelület-IP-konfigurációhoz tartozó terheléselosztási háttércímkészlet-hivatkozások gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="1d318-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="1d318-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="1d318-137">A terhelésegyenleg-elegyenlő bejövő natszabály azon hivatkozásának gyűjteményét adja meg, amelyhez a hálózati felület IPConfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="1d318-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="1d318-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="1d318-139">Azt a terheléselosztási bejövő hálózati címfordítási (NAT-) szabályhivatkozást adja meg, amelyhez ez a hálózatifelület-IP-konfiguráció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d318-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="1d318-140">-Name</span><span class="sxs-lookup"><span data-stu-id="1d318-140">-Name</span></span>
<span data-ttu-id="1d318-141">A hálózati felület IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d318-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="1d318-142">-Primary</span><span class="sxs-lookup"><span data-stu-id="1d318-142">-Primary</span></span>
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

### <span data-ttu-id="1d318-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="1d318-143">-PrivateIpAddress</span></span>
<span data-ttu-id="1d318-144">A hálózati felület IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d318-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="1d318-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="1d318-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="1d318-146">Egy hálózatifelület-IP-konfiguráció IP-címének IP-verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d318-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="1d318-147">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="1d318-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d318-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="1d318-148">IPv4</span></span>
- <span data-ttu-id="1d318-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="1d318-149">IPv6</span></span>

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

### <span data-ttu-id="1d318-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1d318-150">-PublicIpAddress</span></span>
<span data-ttu-id="1d318-151">Egy **PublicIPAddress objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="1d318-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="1d318-152">Ez a parancsmag egy nyilvános IP-címre hivatkozik, és ezzel a hálózatifelület-IP-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="1d318-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="1d318-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="1d318-153">-PublicIpAddressId</span></span>
<span data-ttu-id="1d318-154">Ez a parancsmag egy nyilvános IP-címre hivatkozik, és ezzel a hálózatifelület-IP-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="1d318-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="1d318-155">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="1d318-155">-Subnet</span></span>
<span data-ttu-id="1d318-156">**Alhálózati objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="1d318-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="1d318-157">Ez a parancsmag egy alhálózatra hivatkozik, amelyben létrejön a hálózati felület IP-konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="1d318-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="1d318-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1d318-158">-SubnetId</span></span>
<span data-ttu-id="1d318-159">Annak az alhálózatnak a hivatkozását adja meg, amelyen létrejön ez a hálózatifelület-IP-konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="1d318-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="1d318-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d318-160">CommonParameters</span></span>
<span data-ttu-id="1d318-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d318-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d318-162">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d318-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d318-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d318-163">INPUTS</span></span>

### <span data-ttu-id="1d318-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1d318-164">System.String[]</span></span>

### <span data-ttu-id="1d318-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="1d318-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="1d318-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="1d318-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="1d318-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="1d318-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="1d318-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="1d318-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="1d318-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d318-169">OUTPUTS</span></span>

### <span data-ttu-id="1d318-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d318-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="1d318-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d318-171">NOTES</span></span>
* <span data-ttu-id="1d318-172">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="1d318-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1d318-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d318-173">RELATED LINKS</span></span>

[<span data-ttu-id="1d318-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d318-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1d318-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d318-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1d318-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d318-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1d318-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d318-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
