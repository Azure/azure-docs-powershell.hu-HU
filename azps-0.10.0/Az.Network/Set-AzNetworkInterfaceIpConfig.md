---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0e74aa06d2966ed4e907de7428ddc1f4d3a6f2cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843609"
---
# <span data-ttu-id="7e13a-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e13a-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="7e13a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e13a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e13a-103">Az Azure-alapú hálózati kapcsolat IP-konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="7e13a-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="7e13a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e13a-104">SYNTAX</span></span>

### <span data-ttu-id="7e13a-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e13a-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e13a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e13a-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e13a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e13a-107">DESCRIPTION</span></span>
<span data-ttu-id="7e13a-108">A **set-AzNetworkInterfaceIpConfig** parancsmag az Azure-alapú hálózati kapcsolat IP-konfigurációjának cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="7e13a-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="7e13a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7e13a-109">EXAMPLES</span></span>

### <span data-ttu-id="7e13a-110">1: IP-konfiguráció IP-címének módosítása</span><span class="sxs-lookup"><span data-stu-id="7e13a-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7e13a-111">Az első két parancs a myvnet nevű virtuális hálózatot és egy mysubnet nevű alhálózatot hoz létre, és tárolja a változók $vnet és $subnet.</span><span class="sxs-lookup"><span data-stu-id="7e13a-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="7e13a-112">A harmadik parancs a frissíteni kívánt IP-konfigurációhoz társított hálózati felület nic1 kapja.</span><span class="sxs-lookup"><span data-stu-id="7e13a-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7e13a-113">A harmadik parancs a 10.0.0.11 elsődleges IP-konfigurációs ipconfig1 privát IP-címét állítja be.</span><span class="sxs-lookup"><span data-stu-id="7e13a-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="7e13a-114">Végül az utolsó parancs frissíti azt a hálózati felületet, amely biztosítja a módosítások sikeres létrejöttét.</span><span class="sxs-lookup"><span data-stu-id="7e13a-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="7e13a-115">2: IP-konfiguráció társítása alkalmazások biztonsági groupp</span><span class="sxs-lookup"><span data-stu-id="7e13a-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7e13a-116">Ebben a példában az $asg változó egy alkalmazás biztonsági csoportjának hivatkozását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7e13a-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="7e13a-117">A negyedik parancs a frissíteni kívánt IP-konfigurációhoz társított hálózati felület nic1 kapja.</span><span class="sxs-lookup"><span data-stu-id="7e13a-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7e13a-118">A Set-AzNetworkInterfaceIpConfig az elsődleges IP-konfigurációs ipconfig1 privát IP-címét állítja be a 10.0.0.11, és létrehoz egy társítást a lekérdezett alkalmazás biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="7e13a-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="7e13a-119">Végül az utolsó parancs frissíti azt a hálózati felületet, amely biztosítja a módosítások sikeres létrejöttét.</span><span class="sxs-lookup"><span data-stu-id="7e13a-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="7e13a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e13a-120">PARAMETERS</span></span>

### <span data-ttu-id="7e13a-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7e13a-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7e13a-122">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7e13a-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7e13a-124">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7e13a-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7e13a-126">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7e13a-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7e13a-128">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e13a-129">-DefaultProfile</span></span>
<span data-ttu-id="7e13a-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e13a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e13a-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7e13a-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7e13a-132">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7e13a-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7e13a-134">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7e13a-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7e13a-136">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7e13a-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7e13a-138">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e13a-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7e13a-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e13a-139">-Name</span></span>
<span data-ttu-id="7e13a-140">Annak a hálózatnak az IP-konfigurációjának a neve, amelyhez a parancsmag be van jelölve.</span><span class="sxs-lookup"><span data-stu-id="7e13a-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="7e13a-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7e13a-141">-NetworkInterface</span></span>
<span data-ttu-id="7e13a-142">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7e13a-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="7e13a-143">Ez a parancsmag a hálózati kapcsolat IP-konfigurációját hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="7e13a-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e13a-144">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="7e13a-144">-Primary</span></span>
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

### <span data-ttu-id="7e13a-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e13a-145">-PrivateIpAddress</span></span>
<span data-ttu-id="7e13a-146">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e13a-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="7e13a-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7e13a-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7e13a-148">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e13a-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="7e13a-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7e13a-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e13a-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="7e13a-150">IPv4</span></span>
- <span data-ttu-id="7e13a-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="7e13a-151">IPv6</span></span>

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

### <span data-ttu-id="7e13a-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e13a-152">-PublicIpAddress</span></span>
<span data-ttu-id="7e13a-153">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7e13a-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="7e13a-154">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="7e13a-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7e13a-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7e13a-155">-PublicIpAddressId</span></span>
<span data-ttu-id="7e13a-156">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="7e13a-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7e13a-157">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="7e13a-157">-Subnet</span></span>
<span data-ttu-id="7e13a-158">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7e13a-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7e13a-159">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="7e13a-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7e13a-160">– NetI</span><span class="sxs-lookup"><span data-stu-id="7e13a-160">-SubnetId</span></span>
<span data-ttu-id="7e13a-161">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="7e13a-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7e13a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e13a-162">CommonParameters</span></span>
<span data-ttu-id="7e13a-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e13a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e13a-164">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e13a-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e13a-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e13a-165">INPUTS</span></span>

### <span data-ttu-id="7e13a-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7e13a-166">PSNetworkInterface</span></span>
<span data-ttu-id="7e13a-167">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e13a-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="7e13a-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e13a-168">OUTPUTS</span></span>

### <span data-ttu-id="7e13a-169">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7e13a-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7e13a-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e13a-170">NOTES</span></span>
* <span data-ttu-id="7e13a-171">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="7e13a-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7e13a-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e13a-172">RELATED LINKS</span></span>

[<span data-ttu-id="7e13a-173">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e13a-173">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7e13a-174">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e13a-174">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7e13a-175">Új – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e13a-175">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7e13a-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e13a-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)


