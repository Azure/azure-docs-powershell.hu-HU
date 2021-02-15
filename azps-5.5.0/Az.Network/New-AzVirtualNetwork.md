---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159067"
---
# <span data-ttu-id="cd685-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd685-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="cd685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd685-102">SYNOPSIS</span></span>
<span data-ttu-id="cd685-103">Virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cd685-103">Creates a virtual network.</span></span>

## <span data-ttu-id="cd685-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd685-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd685-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd685-105">DESCRIPTION</span></span>
<span data-ttu-id="cd685-106">A **New-AzVirtualNetwork** parancsmag létrehoz egy Azure virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="cd685-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="cd685-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd685-107">EXAMPLES</span></span>

### <span data-ttu-id="cd685-108">1. példa: Virtuális hálózat létrehozása két alhálózattal</span><span class="sxs-lookup"><span data-stu-id="cd685-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="cd685-109">Ez a példa létrehoz egy virtuális hálózatot két alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="cd685-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="cd685-110">Először egy új erőforráscsoport jön létre a központi régióban.</span><span class="sxs-lookup"><span data-stu-id="cd685-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="cd685-111">Ezután a példa két alhálózatot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="cd685-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="cd685-112">A New-AzVirtualNetworkSubnetConfig parancsmag nem hoz létre alhálózatot a kiszolgálóoldalon.</span><span class="sxs-lookup"><span data-stu-id="cd685-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="cd685-113">Van egy frontendSubnet nevű alhálózat és egy backendSubnet nevű alhálózat.</span><span class="sxs-lookup"><span data-stu-id="cd685-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="cd685-114">A New-AzVirtualNetwork ezt követően létrehoz egy virtuális hálózatot a CIDR 10.0.0.0/16 címelőtag és két alhálózat használatával.</span><span class="sxs-lookup"><span data-stu-id="cd685-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="cd685-115">2. példa: Virtuális hálózat létrehozása DNS-beállításokkal</span><span class="sxs-lookup"><span data-stu-id="cd685-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="cd685-116">Az alábbi példa egy virtuális hálózatot hoz létre két alhálózattal és két DNS-kiszolgálóval.</span><span class="sxs-lookup"><span data-stu-id="cd685-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="cd685-117">A DNS-kiszolgálók virtuális hálózaton való megadásának hatása az, hogy a virtuális hálózatba telepített NICs/VMs az alapértelmezettként örökli ezeket a DNS-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="cd685-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="cd685-118">Ezeket az alapértelmezett értékeket NIC-enként felülírhatja egy NIC-szintű beállítással.</span><span class="sxs-lookup"><span data-stu-id="cd685-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="cd685-119">Ha a VNET nem ad meg DNS-kiszolgálókat, a NIC-n pedig nem, akkor az alapértelmezett Azure DNS-kiszolgálók használhatók a DNS-feloldáshoz.</span><span class="sxs-lookup"><span data-stu-id="cd685-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="cd685-120">3. példa: Virtuális hálózat létrehozása hálózati biztonsági csoportra hivatkozó alhálózattal</span><span class="sxs-lookup"><span data-stu-id="cd685-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="cd685-121">Ez a példa létrehoz egy virtuális hálózatot, amely egy hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="cd685-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="cd685-122">Első lépésként a példa létrehoz egy erőforráscsoportot a létrehozatott erőforrások tárolójaként.</span><span class="sxs-lookup"><span data-stu-id="cd685-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="cd685-123">Ezután létrejön egy olyan hálózati biztonsági csoport, amely lehetővé teszi a bejövő RDP-hozzáférést, de más módon érvényesíti a hálózat biztonsági csoport alapértelmezett szabályait.</span><span class="sxs-lookup"><span data-stu-id="cd685-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="cd685-124">A New-AzVirtualNetworkSubnetConfig ezt követően két alhálózat memóriában való megjelenítését hozza létre, amelyek a létrehozott hálózati biztonsági csoportra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="cd685-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="cd685-125">A New-AzVirtualNetwork parancsot, majd létrehozza a virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="cd685-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="cd685-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd685-126">PARAMETERS</span></span>

### <span data-ttu-id="cd685-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cd685-127">-AddressPrefix</span></span>
<span data-ttu-id="cd685-128">Egy virtuális hálózat IP-címtartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd685-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="cd685-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd685-129">-AsJob</span></span>
<span data-ttu-id="cd685-130">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd685-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd685-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="cd685-131">-BgpCommunity</span></span>
<span data-ttu-id="cd685-132">Az ExpressRoute-on keresztül meghirdetett BGP-közösség.</span><span class="sxs-lookup"><span data-stu-id="cd685-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="cd685-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="cd685-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="cd685-134">Hivatkozás a virtuális hálózathoz társított DDoS védelmi terv erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="cd685-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="cd685-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd685-135">-DefaultProfile</span></span>
<span data-ttu-id="cd685-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd685-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd685-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="cd685-137">-DnsServer</span></span>
<span data-ttu-id="cd685-138">Egy alhálózat DNS-kiszolgálóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd685-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="cd685-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="cd685-139">-EnableDdosProtection</span></span>
<span data-ttu-id="cd685-140">A kapcsoló paramétere, amely azt jelzi, hogy a DDoS-védelem engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="cd685-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="cd685-141">-Force</span><span class="sxs-lookup"><span data-stu-id="cd685-141">-Force</span></span>
<span data-ttu-id="cd685-142">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cd685-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd685-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="cd685-143">-IpAllocation</span></span>
<span data-ttu-id="cd685-144">IpAllocations megadása virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="cd685-144">Specifies IpAllocations for a virtual network.</span></span>

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

### <span data-ttu-id="cd685-145">-Location</span><span class="sxs-lookup"><span data-stu-id="cd685-145">-Location</span></span>
<span data-ttu-id="cd685-146">A virtuális hálózat régióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd685-146">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="cd685-147">-Name</span><span class="sxs-lookup"><span data-stu-id="cd685-147">-Name</span></span>
<span data-ttu-id="cd685-148">A parancsmag által létrehozott virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="cd685-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cd685-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd685-149">-ResourceGroupName</span></span>
<span data-ttu-id="cd685-150">A virtuális hálózatot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd685-150">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="cd685-151">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="cd685-151">-Subnet</span></span>
<span data-ttu-id="cd685-152">Megadja a virtuális hálózattal társítva lévő alhálózatok listáját.</span><span class="sxs-lookup"><span data-stu-id="cd685-152">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="cd685-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd685-153">-Tag</span></span>
<span data-ttu-id="cd685-154">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="cd685-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd685-155">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="cd685-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cd685-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd685-156">-Confirm</span></span>
<span data-ttu-id="cd685-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd685-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd685-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd685-158">-WhatIf</span></span>
<span data-ttu-id="cd685-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd685-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd685-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd685-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd685-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd685-161">CommonParameters</span></span>
<span data-ttu-id="cd685-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd685-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd685-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd685-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd685-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd685-164">INPUTS</span></span>

### <span data-ttu-id="cd685-165">System.String</span><span class="sxs-lookup"><span data-stu-id="cd685-165">System.String</span></span>

### <span data-ttu-id="cd685-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cd685-166">System.String[]</span></span>

### <span data-ttu-id="cd685-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="cd685-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="cd685-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd685-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cd685-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd685-169">OUTPUTS</span></span>

### <span data-ttu-id="cd685-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd685-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cd685-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd685-171">NOTES</span></span>

## <span data-ttu-id="cd685-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd685-172">RELATED LINKS</span></span>

[<span data-ttu-id="cd685-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd685-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="cd685-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd685-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="cd685-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd685-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="cd685-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="cd685-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
