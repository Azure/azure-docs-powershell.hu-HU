---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184357"
---
# <span data-ttu-id="280f5-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="280f5-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="280f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="280f5-102">SYNOPSIS</span></span>
<span data-ttu-id="280f5-103">Virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="280f5-103">Creates a virtual network.</span></span>

## <span data-ttu-id="280f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="280f5-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="280f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="280f5-105">DESCRIPTION</span></span>
<span data-ttu-id="280f5-106">A **New-AzVirtualNetwork** parancsmag egy Azure virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="280f5-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="280f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="280f5-107">EXAMPLES</span></span>

### <span data-ttu-id="280f5-108">Példa 1: virtuális hálózat létrehozása két alhálózattal</span><span class="sxs-lookup"><span data-stu-id="280f5-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="280f5-109">Ebben a példában két alhálózatot tartalmazó virtuális hálózat jön létre.</span><span class="sxs-lookup"><span data-stu-id="280f5-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="280f5-110">Először egy új erőforráscsoport jön létre a CentralUS-régióban.</span><span class="sxs-lookup"><span data-stu-id="280f5-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="280f5-111">Ezután a példa két alhálózat memóriában ábrázolt példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="280f5-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="280f5-112">A New-AzVirtualNetworkSubnetConfig parancsmag nem hoz létre alhálózatokat a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="280f5-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="280f5-113">Egy frontendSubnet nevű alhálózatot és egy backendSubnet nevű alhálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="280f5-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="280f5-114">A New-AzVirtualNetwork parancsmag ezután virtuális hálózatot hoz létre a CIDR 10.0.0.0/16 segítségével a cím előtagként és két alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="280f5-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="280f5-115">2. példa: virtuális hálózat létrehozása a DNS-beállításokkal</span><span class="sxs-lookup"><span data-stu-id="280f5-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="280f5-116">Ebben a példában egy virtuális hálózat jön létre két alhálózattal és két DNS-kiszolgálóval.</span><span class="sxs-lookup"><span data-stu-id="280f5-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="280f5-117">A DNS-kiszolgálók virtuális hálózaton való megadásának hatásai az, hogy a virtuális hálózatba telepített hálózati adapterek/VMs-kiszolgálók alapértelmezés szerint öröklik ezeket a DNS-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="280f5-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="280f5-118">Ezek az alapértelmezett beállítások a NIC-es hálózati adapteren keresztül felülíródnak.</span><span class="sxs-lookup"><span data-stu-id="280f5-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="280f5-119">Ha a VNET nem ad meg DNS-kiszolgálókat, és nem a hálózati adaptereken, akkor az alapértelmezett Azure DNS-kiszolgálók használhatók a DNS-feloldáshoz.</span><span class="sxs-lookup"><span data-stu-id="280f5-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="280f5-120">3. példa: virtuális hálózat létrehozása hálózati biztonsági csoportra hivatkozó alhálózattal</span><span class="sxs-lookup"><span data-stu-id="280f5-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="280f5-121">Ez a példa virtuális hálózatot hoz létre olyan alhálózatokkal, amelyek hálózati biztonsági csoportra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="280f5-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="280f5-122">Először a példa létrehoz egy erőforráscsoportot tárolóként a létrehozandó erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="280f5-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="280f5-123">Ezután egy hálózati biztonsági csoport jön létre, amely lehetővé teszi a bejövő RDP-elérést, de egyéb módon kényszeríti az alapértelmezett hálózati biztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="280f5-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="280f5-124">A New-AzVirtualNetworkSubnetConfig parancsmag két alhálózat memóriában ábrázolt példányait hozza létre, amelyek a létrehozott hálózati biztonsági csoportra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="280f5-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="280f5-125">A New-AzVirtualNetwork parancs a virtuális hálózatot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="280f5-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="280f5-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="280f5-126">PARAMETERS</span></span>

### <span data-ttu-id="280f5-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="280f5-127">-AddressPrefix</span></span>
<span data-ttu-id="280f5-128">Egy virtuális hálózat IP-címeinek egy-egy IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="280f5-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="280f5-129">-AsJob</span></span>
<span data-ttu-id="280f5-130">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="280f5-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="280f5-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="280f5-131">-BgpCommunity</span></span>
<span data-ttu-id="280f5-132">A BGP-Közösség hirdetett át a ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="280f5-132">The BGP Community advertised over ExpressRoute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="280f5-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="280f5-134">Hivatkozás a virtuális hálózathoz társított DDoS védelmi terv erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="280f5-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280f5-135">-DefaultProfile</span></span>
<span data-ttu-id="280f5-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="280f5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="280f5-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="280f5-137">-DnsServer</span></span>
<span data-ttu-id="280f5-138">Az alhálózat DNS-kiszolgálóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="280f5-138">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="280f5-139">-EnableDdosProtection</span></span>
<span data-ttu-id="280f5-140">Egy kapcsoló paraméter, amely akkor jelenik meg, ha a DDoS védelem engedélyezve van vagy nem.</span><span class="sxs-lookup"><span data-stu-id="280f5-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-141">-Force</span><span class="sxs-lookup"><span data-stu-id="280f5-141">-Force</span></span>
<span data-ttu-id="280f5-142">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="280f5-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="280f5-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="280f5-143">-IpAllocation</span></span>
<span data-ttu-id="280f5-144">A virtuális hálózat IpAllocations adja meg.</span><span class="sxs-lookup"><span data-stu-id="280f5-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="280f5-145">-Location</span></span>
<span data-ttu-id="280f5-146">A virtuális hálózat területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="280f5-146">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="280f5-147">-Name</span></span>
<span data-ttu-id="280f5-148">Annak a virtuális hálózatnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="280f5-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280f5-149">-ResourceGroupName</span></span>
<span data-ttu-id="280f5-150">A virtuális hálózatot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="280f5-150">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-151">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="280f5-151">-Subnet</span></span>
<span data-ttu-id="280f5-152">A virtuális hálózattal társítani kívánt alhálózatok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="280f5-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-153">-Címke</span><span class="sxs-lookup"><span data-stu-id="280f5-153">-Tag</span></span>
<span data-ttu-id="280f5-154">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="280f5-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="280f5-155">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="280f5-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="280f5-156">-Confirm</span></span>
<span data-ttu-id="280f5-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="280f5-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="280f5-158">-WhatIf</span></span>
<span data-ttu-id="280f5-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="280f5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="280f5-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="280f5-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280f5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280f5-161">CommonParameters</span></span>
<span data-ttu-id="280f5-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="280f5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280f5-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="280f5-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280f5-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="280f5-164">INPUTS</span></span>

### <span data-ttu-id="280f5-165">System. String</span><span class="sxs-lookup"><span data-stu-id="280f5-165">System.String</span></span>

### <span data-ttu-id="280f5-166">System. string []</span><span class="sxs-lookup"><span data-stu-id="280f5-166">System.String[]</span></span>

### <span data-ttu-id="280f5-167">Microsoft. Azure. commands. Network. models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="280f5-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="280f5-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="280f5-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="280f5-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="280f5-169">OUTPUTS</span></span>

### <span data-ttu-id="280f5-170">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="280f5-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="280f5-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="280f5-171">NOTES</span></span>

## <span data-ttu-id="280f5-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="280f5-172">RELATED LINKS</span></span>

[<span data-ttu-id="280f5-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="280f5-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="280f5-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="280f5-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="280f5-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="280f5-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="280f5-176">Új – AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="280f5-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
