---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184890"
---
# <span data-ttu-id="a89ae-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a89ae-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a89ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a89ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a89ae-103">Hálózati biztonsági szabály konfigurációjának felvétele hálózati biztonsági csoportba.</span><span class="sxs-lookup"><span data-stu-id="a89ae-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="a89ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a89ae-104">SYNTAX</span></span>

### <span data-ttu-id="a89ae-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a89ae-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a89ae-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a89ae-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a89ae-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a89ae-107">DESCRIPTION</span></span>
<span data-ttu-id="a89ae-108">Az **Add-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály-konfigurációt ad hozzá az Azure hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="a89ae-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="a89ae-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a89ae-109">EXAMPLES</span></span>

### <span data-ttu-id="a89ae-110">1: hálózati biztonsági csoport hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a89ae-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="a89ae-111">Az első parancs a "rg1" erőforráscsoport "nsg1" nevű Azure hálózati biztonsági csoportjának beolvasása.</span><span class="sxs-lookup"><span data-stu-id="a89ae-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="a89ae-112">A második parancs hozzáadja az "RDP-szabály" nevű hálózati biztonsági szabályt, amely lehetővé teszi, hogy a 3389-on lévő internetről érkező forgalom a lekérdezett hálózati biztonsági csoport objektumba kerüljön.</span><span class="sxs-lookup"><span data-stu-id="a89ae-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="a89ae-113">Megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="a89ae-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="a89ae-114">2: új biztonsági szabály felvétele az alkalmazás biztonsági csoportjaival</span><span class="sxs-lookup"><span data-stu-id="a89ae-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="a89ae-115">Elsőként hozzunk létre két új alkalmazás biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="a89ae-115">First, we create two new application security groups.</span></span> <span data-ttu-id="a89ae-116">Ezután egy "nsg1" nevű Azure Network biztonsági csoportot keresünk a "rg1" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a89ae-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="a89ae-117">lehetőséget, és adjon hozzá egy "RDP-Rule" nevű hálózati biztonsági szabályt.</span><span class="sxs-lookup"><span data-stu-id="a89ae-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="a89ae-118">A szabály megengedi az összes IP-beállítás forgalmát a "srcAsg" az összes IP-konfigurációból az 3389-es port "destAsg" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="a89ae-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="a89ae-119">Miután hozzáadta a szabályt, továbbra is fennáll a módosított Azure-hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="a89ae-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="a89ae-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a89ae-120">PARAMETERS</span></span>

### <span data-ttu-id="a89ae-121">-Access</span><span class="sxs-lookup"><span data-stu-id="a89ae-121">-Access</span></span>
<span data-ttu-id="a89ae-122">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="a89ae-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="a89ae-123">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="a89ae-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="a89ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89ae-124">-DefaultProfile</span></span>
<span data-ttu-id="a89ae-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a89ae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a89ae-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a89ae-126">-Description</span></span>
<span data-ttu-id="a89ae-127">A hálózati biztonsági szabályok konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="a89ae-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a89ae-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="a89ae-129">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="a89ae-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a89ae-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a89ae-131">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="a89ae-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="a89ae-132">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="a89ae-132">A destination IP address range</span></span>
- <span data-ttu-id="a89ae-133">A helyettesítő karakter (\*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.</span><span class="sxs-lookup"><span data-stu-id="a89ae-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="a89ae-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a89ae-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="a89ae-135">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="a89ae-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a89ae-136">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="a89ae-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a89ae-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a89ae-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="a89ae-138">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="a89ae-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a89ae-139">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="a89ae-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a89ae-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="a89ae-140">-DestinationPortRange</span></span>
<span data-ttu-id="a89ae-141">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="a89ae-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a89ae-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a89ae-143">Egész szám</span><span class="sxs-lookup"><span data-stu-id="a89ae-143">An integer</span></span>
- <span data-ttu-id="a89ae-144">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="a89ae-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a89ae-145">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="a89ae-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a89ae-146">-Irány</span><span class="sxs-lookup"><span data-stu-id="a89ae-146">-Direction</span></span>
<span data-ttu-id="a89ae-147">Azt adja meg, hogy a rendszer kiértékeli-e a szabályt a bejövő vagy kimenő forgalomban.</span><span class="sxs-lookup"><span data-stu-id="a89ae-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="a89ae-148">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="a89ae-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="a89ae-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a89ae-149">-Name</span></span>
<span data-ttu-id="a89ae-150">A hálózati biztonsági szabályok konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="a89ae-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a89ae-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a89ae-152">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="a89ae-153">Ez a parancsmag hálózati biztonsági szabály konfigurációját adja hozzá az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="a89ae-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="a89ae-154">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="a89ae-154">-Priority</span></span>
<span data-ttu-id="a89ae-155">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="a89ae-156">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="a89ae-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="a89ae-157">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="a89ae-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="a89ae-158">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="a89ae-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="a89ae-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a89ae-159">-Protocol</span></span>
<span data-ttu-id="a89ae-160">Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="a89ae-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="a89ae-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a89ae-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a89ae-162">TCP</span><span class="sxs-lookup"><span data-stu-id="a89ae-162">Tcp</span></span>
- <span data-ttu-id="a89ae-163">UDP</span><span class="sxs-lookup"><span data-stu-id="a89ae-163">Udp</span></span>
- <span data-ttu-id="a89ae-164">Helyettesítő karakter (\*) a két érték egyeztetéséhez</span><span class="sxs-lookup"><span data-stu-id="a89ae-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="a89ae-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a89ae-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="a89ae-166">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="a89ae-167">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a89ae-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a89ae-168">CIDR</span><span class="sxs-lookup"><span data-stu-id="a89ae-168">A CIDR</span></span>
- <span data-ttu-id="a89ae-169">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="a89ae-169">A source IP range</span></span>
- <span data-ttu-id="a89ae-170">Egy helyettesítő karakter (\*) az IP-cím megegyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="a89ae-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="a89ae-171">A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.</span><span class="sxs-lookup"><span data-stu-id="a89ae-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="a89ae-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a89ae-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="a89ae-173">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="a89ae-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="a89ae-174">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="a89ae-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a89ae-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a89ae-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="a89ae-176">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="a89ae-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="a89ae-177">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="a89ae-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a89ae-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="a89ae-178">-SourcePortRange</span></span>
<span data-ttu-id="a89ae-179">A forrás-portot vagy-cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ae-179">Specifies a source port or range.</span></span>
<span data-ttu-id="a89ae-180">Ezt az értéket egész számként fejezi ki, 0 és 65535 közötti tartománnyal, vagy helyettesítő karakterként (\*), amely a forrás-porthoz igazodik.</span><span class="sxs-lookup"><span data-stu-id="a89ae-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="a89ae-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89ae-181">CommonParameters</span></span>
<span data-ttu-id="a89ae-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a89ae-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89ae-183">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89ae-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89ae-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a89ae-184">INPUTS</span></span>

### <span data-ttu-id="a89ae-185">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a89ae-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a89ae-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a89ae-186">OUTPUTS</span></span>

### <span data-ttu-id="a89ae-187">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a89ae-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a89ae-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a89ae-188">NOTES</span></span>

## <span data-ttu-id="a89ae-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a89ae-189">RELATED LINKS</span></span>

[<span data-ttu-id="a89ae-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a89ae-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a89ae-191">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a89ae-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a89ae-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a89ae-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a89ae-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a89ae-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

