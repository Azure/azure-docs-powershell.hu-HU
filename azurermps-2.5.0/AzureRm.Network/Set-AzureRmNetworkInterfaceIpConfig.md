---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: f37f6fe6211ab05b94249b924eb76c4b98d05082
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850301"
---
# <span data-ttu-id="b36fb-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b36fb-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="b36fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b36fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b36fb-103">Az Azure-alapú hálózati kapcsolat IP-konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="b36fb-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b36fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b36fb-104">SYNTAX</span></span>

### <span data-ttu-id="b36fb-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b36fb-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b36fb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b36fb-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b36fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b36fb-107">DESCRIPTION</span></span>
<span data-ttu-id="b36fb-108">A **set-AzureRmNetworkInterfaceIpConfig** parancsmag az Azure-alapú hálózati kapcsolat IP-konfigurációjának cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="b36fb-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="b36fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b36fb-109">EXAMPLES</span></span>

### <span data-ttu-id="b36fb-110">1: IP-konfiguráció IP-címének módosítása</span><span class="sxs-lookup"><span data-stu-id="b36fb-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b36fb-111">Az első két parancs a myvnet nevű virtuális hálózatot és egy mysubnet nevű alhálózatot hoz létre, és tárolja a változók $vnet és $subnet.</span><span class="sxs-lookup"><span data-stu-id="b36fb-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="b36fb-112">A harmadik parancs a frissíteni kívánt IP-konfigurációhoz társított hálózati felület nic1 kapja.</span><span class="sxs-lookup"><span data-stu-id="b36fb-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b36fb-113">A harmadik parancs a 10.0.0.11 elsődleges IP-konfigurációs ipconfig1 privát IP-címét állítja be.</span><span class="sxs-lookup"><span data-stu-id="b36fb-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="b36fb-114">Végül az utolsó parancs frissíti azt a hálózati felületet, amely biztosítja a módosítások sikeres létrejöttét.</span><span class="sxs-lookup"><span data-stu-id="b36fb-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="b36fb-115">2: IP-konfiguráció társítása alkalmazások biztonsági groupp</span><span class="sxs-lookup"><span data-stu-id="b36fb-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b36fb-116">Ebben a példában az $asg változó egy alkalmazás biztonsági csoportjának hivatkozását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b36fb-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="b36fb-117">A negyedik parancs a frissíteni kívánt IP-konfigurációhoz társított hálózati felület nic1 kapja.</span><span class="sxs-lookup"><span data-stu-id="b36fb-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b36fb-118">A Set-AzureRmNetworkInterfaceIpConfig az elsődleges IP-konfigurációs ipconfig1 privát IP-címét állítja be a 10.0.0.11, és létrehoz egy társítást a lekérdezett alkalmazás biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="b36fb-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="b36fb-119">Végül az utolsó parancs frissíti azt a hálózati felületet, amely biztosítja a módosítások sikeres létrejöttét.</span><span class="sxs-lookup"><span data-stu-id="b36fb-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="b36fb-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b36fb-120">PARAMETERS</span></span>

### <span data-ttu-id="b36fb-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b36fb-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b36fb-122">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b36fb-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b36fb-124">Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b36fb-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b36fb-126">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b36fb-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b36fb-128">Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36fb-129">-DefaultProfile</span></span>
<span data-ttu-id="b36fb-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b36fb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36fb-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b36fb-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b36fb-132">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b36fb-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b36fb-134">A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b36fb-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b36fb-136">A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="b36fb-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b36fb-138">A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.</span><span class="sxs-lookup"><span data-stu-id="b36fb-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b36fb-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b36fb-139">-Name</span></span>
<span data-ttu-id="b36fb-140">Annak a hálózatnak az IP-konfigurációjának a neve, amelyhez a parancsmag be van jelölve.</span><span class="sxs-lookup"><span data-stu-id="b36fb-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="b36fb-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b36fb-141">-NetworkInterface</span></span>
<span data-ttu-id="b36fb-142">Egy **NetworkInterface** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b36fb-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="b36fb-143">Ez a parancsmag a hálózati kapcsolat IP-konfigurációját hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="b36fb-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b36fb-144">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="b36fb-144">-Primary</span></span>
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

### <span data-ttu-id="b36fb-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b36fb-145">-PrivateIpAddress</span></span>
<span data-ttu-id="b36fb-146">A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b36fb-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="b36fb-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b36fb-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b36fb-148">A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b36fb-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="b36fb-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b36fb-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b36fb-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="b36fb-150">IPv4</span></span>
- <span data-ttu-id="b36fb-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="b36fb-151">IPv6</span></span>

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

### <span data-ttu-id="b36fb-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b36fb-152">-PublicIpAddress</span></span>
<span data-ttu-id="b36fb-153">Egy **PublicIPAddress** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b36fb-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="b36fb-154">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="b36fb-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b36fb-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b36fb-155">-PublicIpAddressId</span></span>
<span data-ttu-id="b36fb-156">Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.</span><span class="sxs-lookup"><span data-stu-id="b36fb-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b36fb-157">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="b36fb-157">-Subnet</span></span>
<span data-ttu-id="b36fb-158">**Alhálózat** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b36fb-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b36fb-159">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="b36fb-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b36fb-160">– NetI</span><span class="sxs-lookup"><span data-stu-id="b36fb-160">-SubnetId</span></span>
<span data-ttu-id="b36fb-161">Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.</span><span class="sxs-lookup"><span data-stu-id="b36fb-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b36fb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36fb-162">CommonParameters</span></span>
<span data-ttu-id="b36fb-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b36fb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36fb-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b36fb-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36fb-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b36fb-165">INPUTS</span></span>

### <span data-ttu-id="b36fb-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b36fb-166">PSNetworkInterface</span></span>
<span data-ttu-id="b36fb-167">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b36fb-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="b36fb-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b36fb-168">OUTPUTS</span></span>

### <span data-ttu-id="b36fb-169">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b36fb-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b36fb-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b36fb-170">NOTES</span></span>
* <span data-ttu-id="b36fb-171">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="b36fb-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b36fb-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b36fb-172">RELATED LINKS</span></span>

[<span data-ttu-id="b36fb-173">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b36fb-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b36fb-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b36fb-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b36fb-175">Új – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b36fb-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b36fb-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b36fb-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


