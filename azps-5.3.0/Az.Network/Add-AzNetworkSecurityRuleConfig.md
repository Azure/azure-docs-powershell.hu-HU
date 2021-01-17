---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467446"
---
# <span data-ttu-id="65ed4-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65ed4-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="65ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="65ed4-103">Hálózati biztonsági szabály konfigurációját ad hozzá egy hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="65ed4-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="65ed4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65ed4-104">SYNTAX</span></span>

### <span data-ttu-id="65ed4-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65ed4-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65ed4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65ed4-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65ed4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65ed4-107">DESCRIPTION</span></span>
<span data-ttu-id="65ed4-108">Az **Add-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabálykonfigurációt ad egy Azure-hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="65ed4-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="65ed4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65ed4-109">EXAMPLES</span></span>

### <span data-ttu-id="65ed4-110">1: Hálózati biztonsági csoport hozzáadása</span><span class="sxs-lookup"><span data-stu-id="65ed4-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="65ed4-111">Az első parancs lekéri az "rg1" erőforráscsoportból az "nsg1" nevű Azure-hálózat biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="65ed4-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="65ed4-112">A második parancs hozzáad egy "rdp-rule" nevű hálózati biztonsági szabályt, amely lehetővé teszi az internetről a 3389-es porton keresztüli forgalmat a lekért hálózati biztonsági csoport objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="65ed4-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="65ed4-113">A módosított Azure-hálózat biztonsági csoport megőrzve.</span><span class="sxs-lookup"><span data-stu-id="65ed4-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="65ed4-114">2: Új biztonsági szabály hozzáadása alkalmazásbiztonsági csoportokkal</span><span class="sxs-lookup"><span data-stu-id="65ed4-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="65ed4-115">Először két új alkalmazásbiztonsági csoportot hozunk létre.</span><span class="sxs-lookup"><span data-stu-id="65ed4-115">First, we create two new application security groups.</span></span> <span data-ttu-id="65ed4-116">Ezután lekérünk egy "nsg1" nevű Azure-hálózatbiztonsági csoportot az "rg1" erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="65ed4-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="65ed4-117">és adjon hozzá egy "rdp-rule" nevű hálózati biztonsági szabályt.</span><span class="sxs-lookup"><span data-stu-id="65ed4-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="65ed4-118">A szabály lehetővé teszi az "srcAsg" alkalmazásbiztonsági csoport összes IP-konfigurációjából a 3389-es porton található "destAsg" IP-konfigurációkba való forgalmat.</span><span class="sxs-lookup"><span data-stu-id="65ed4-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="65ed4-119">A szabály hozzáadása után megmarad a módosított Azure-hálózat biztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="65ed4-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="65ed4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65ed4-120">PARAMETERS</span></span>

### <span data-ttu-id="65ed4-121">-Access</span><span class="sxs-lookup"><span data-stu-id="65ed4-121">-Access</span></span>
<span data-ttu-id="65ed4-122">Azt adja meg, hogy engedélyezett vagy megtagadható-e a hálózati forgalom.</span><span class="sxs-lookup"><span data-stu-id="65ed4-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="65ed4-123">A paraméter elfogadható értékei: Allow és Deny.</span><span class="sxs-lookup"><span data-stu-id="65ed4-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ed4-124">-DefaultProfile</span></span>
<span data-ttu-id="65ed4-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65ed4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ed4-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="65ed4-126">-Description</span></span>
<span data-ttu-id="65ed4-127">Megadja egy hálózati biztonsági szabály konfigurációjának leírását.</span><span class="sxs-lookup"><span data-stu-id="65ed4-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="65ed4-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="65ed4-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="65ed4-129">Megadja a célcím előtagját.</span><span class="sxs-lookup"><span data-stu-id="65ed4-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="65ed4-130">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="65ed4-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65ed4-131">A Classless Interdomain Routing (CIDR) address</span><span class="sxs-lookup"><span data-stu-id="65ed4-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="65ed4-132">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="65ed4-132">A destination IP address range</span></span>
- <span data-ttu-id="65ed4-133">Helyettesítő karakter (\*) bármely IP-címhez. Használhat például VirtualNetwork, AzureLoadBalancer és Internet címkéket.</span><span class="sxs-lookup"><span data-stu-id="65ed4-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65ed4-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="65ed4-135">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="65ed4-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="65ed4-136">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="65ed4-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="65ed4-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="65ed4-138">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="65ed4-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="65ed4-139">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="65ed4-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="65ed4-140">-DestinationPortRange</span></span>
<span data-ttu-id="65ed4-141">Célportot vagy tartományt ad meg.</span><span class="sxs-lookup"><span data-stu-id="65ed4-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="65ed4-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="65ed4-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65ed4-143">Egész szám</span><span class="sxs-lookup"><span data-stu-id="65ed4-143">An integer</span></span>
- <span data-ttu-id="65ed4-144">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="65ed4-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="65ed4-145">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="65ed4-145">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-146">-Irány</span><span class="sxs-lookup"><span data-stu-id="65ed4-146">-Direction</span></span>
<span data-ttu-id="65ed4-147">Meghatározza, hogy egy szabály kiértékelve legyen-e a bejövő vagy kimenő forgalom esetén.</span><span class="sxs-lookup"><span data-stu-id="65ed4-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="65ed4-148">A paraméter elfogadható értékei a következőek: Bejövő és Kimenő.</span><span class="sxs-lookup"><span data-stu-id="65ed4-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-149">-Name</span><span class="sxs-lookup"><span data-stu-id="65ed4-149">-Name</span></span>
<span data-ttu-id="65ed4-150">Egy hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65ed4-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="65ed4-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65ed4-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="65ed4-152">**NetworkSecurityGroup-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="65ed4-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="65ed4-153">Ez a parancsmag hálózati biztonsági szabálykonfigurációt ad a paraméterként megadott objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="65ed4-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="65ed4-154">-Priority</span></span>
<span data-ttu-id="65ed4-155">Meghatározza a szabálykonfiguráció prioritását.</span><span class="sxs-lookup"><span data-stu-id="65ed4-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="65ed4-156">A paraméter elfogadható értékei: Egy 100 és 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="65ed4-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="65ed4-157">A prioritásszámnak egyedinek kell lennie a gyűjtemény minden egyes szabályában.</span><span class="sxs-lookup"><span data-stu-id="65ed4-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="65ed4-158">Minél kisebb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="65ed4-158">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="65ed4-159">-Protocol</span></span>
<span data-ttu-id="65ed4-160">Azt a hálózati protokollt adja meg, amelyre a szabálykonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="65ed4-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="65ed4-161">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="65ed4-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65ed4-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="65ed4-162">Tcp</span></span>
- <span data-ttu-id="65ed4-163">Udp</span><span class="sxs-lookup"><span data-stu-id="65ed4-163">Udp</span></span>
- <span data-ttu-id="65ed4-164">Helyettesítő karakter (\*) mindkét karakterhez</span><span class="sxs-lookup"><span data-stu-id="65ed4-164">Wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="65ed4-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="65ed4-166">Megadja a forráscím előtagját.</span><span class="sxs-lookup"><span data-stu-id="65ed4-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="65ed4-167">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="65ed4-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65ed4-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="65ed4-168">A CIDR</span></span>
- <span data-ttu-id="65ed4-169">Forrás IP-tartomány</span><span class="sxs-lookup"><span data-stu-id="65ed4-169">A source IP range</span></span>
- <span data-ttu-id="65ed4-170">Egy tetszőleges IP-címnek megfelelő helyettesítő karakter (\*).</span><span class="sxs-lookup"><span data-stu-id="65ed4-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="65ed4-171">Használhat olyan címkéket is, mint a VirtualNetwork, az AzureLoadBalancer és az internet.</span><span class="sxs-lookup"><span data-stu-id="65ed4-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65ed4-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="65ed4-173">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="65ed4-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="65ed4-174">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="65ed4-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="65ed4-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="65ed4-176">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="65ed4-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="65ed4-177">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="65ed4-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="65ed4-178">-SourcePortRange</span></span>
<span data-ttu-id="65ed4-179">Egy forrásportot vagy -tartományt ad meg.</span><span class="sxs-lookup"><span data-stu-id="65ed4-179">Specifies a source port or range.</span></span>
<span data-ttu-id="65ed4-180">Ez az érték egész számként, 0 és 65535 közötti tartományként, illetve helyettesítő karakterként (\*) fejezi ki, hogy megfeleljen a forrásportok bármelyikének.</span><span class="sxs-lookup"><span data-stu-id="65ed4-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ed4-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ed4-181">CommonParameters</span></span>
<span data-ttu-id="65ed4-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ed4-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ed4-183">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ed4-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ed4-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65ed4-184">INPUTS</span></span>

### <span data-ttu-id="65ed4-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65ed4-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="65ed4-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65ed4-186">OUTPUTS</span></span>

### <span data-ttu-id="65ed4-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65ed4-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="65ed4-188">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65ed4-188">NOTES</span></span>

## <span data-ttu-id="65ed4-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65ed4-189">RELATED LINKS</span></span>

[<span data-ttu-id="65ed4-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65ed4-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="65ed4-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65ed4-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="65ed4-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65ed4-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="65ed4-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65ed4-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


