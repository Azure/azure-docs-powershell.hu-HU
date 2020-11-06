---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 0efe2c4492a9fb91ffd2083c9f23cfc314c2d3fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499796"
---
# <span data-ttu-id="78f83-101">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78f83-101">Add-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="78f83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78f83-102">SYNOPSIS</span></span>
<span data-ttu-id="78f83-103">Hálózati biztonsági szabály konfigurációjának felvétele hálózati biztonsági csoportba.</span><span class="sxs-lookup"><span data-stu-id="78f83-103">Adds a network security rule configuration to a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78f83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78f83-104">SYNTAX</span></span>

### <span data-ttu-id="78f83-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78f83-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78f83-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="78f83-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78f83-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="78f83-107">DESCRIPTION</span></span>
<span data-ttu-id="78f83-108">Az **Add-AzureRmNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály-konfigurációt ad hozzá az Azure hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="78f83-108">The **Add-AzureRmNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="78f83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="78f83-109">EXAMPLES</span></span>

### <span data-ttu-id="78f83-110">1: hálózati biztonsági csoport hozzáadása</span><span class="sxs-lookup"><span data-stu-id="78f83-110">1: Adding a network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="78f83-111">Az első parancs a "rg1" erőforráscsoport "nsg1" nevű Azure hálózati biztonsági csoportjának beolvasása.</span><span class="sxs-lookup"><span data-stu-id="78f83-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="78f83-112">A második parancs hozzáadja az "RDP-szabály" nevű hálózati biztonsági szabályt, amely lehetővé teszi, hogy a 3389-on lévő internetről érkező forgalom a lekérdezett hálózati biztonsági csoport objektumba kerüljön.</span><span class="sxs-lookup"><span data-stu-id="78f83-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="78f83-113">Megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="78f83-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="78f83-114">1: új biztonsági szabály felvétele az alkalmazás biztonsági csoportjaival</span><span class="sxs-lookup"><span data-stu-id="78f83-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="78f83-115">Elsőként hozzunk létre két új alkalmazás biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="78f83-115">First, we create two new application security groups.</span></span> <span data-ttu-id="78f83-116">Ezután egy "nsg1" nevű Azure Network biztonsági csoportot keresünk a "rg1" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="78f83-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="78f83-117">lehetőséget, és adjon hozzá egy "RDP-Rule" nevű hálózati biztonsági szabályt.</span><span class="sxs-lookup"><span data-stu-id="78f83-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="78f83-118">A szabály megengedi az összes IP-beállítás forgalmát a "srcAsg" az összes IP-konfigurációból az 3389-es port "destAsg" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="78f83-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="78f83-119">Miután hozzáadta a szabályt, továbbra is fennáll a módosított Azure-hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="78f83-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="78f83-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78f83-120">PARAMETERS</span></span>

### <span data-ttu-id="78f83-121">-Access</span><span class="sxs-lookup"><span data-stu-id="78f83-121">-Access</span></span>
<span data-ttu-id="78f83-122">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="78f83-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="78f83-123">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="78f83-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f83-124">-DefaultProfile</span></span>
<span data-ttu-id="78f83-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78f83-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78f83-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="78f83-126">-Description</span></span>
<span data-ttu-id="78f83-127">A hálózati biztonsági szabályok konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="78f83-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="78f83-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="78f83-129">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="78f83-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78f83-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78f83-131">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="78f83-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="78f83-132">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="78f83-132">A destination IP address range</span></span>
- <span data-ttu-id="78f83-133">Bármely IP-címnek megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="78f83-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="78f83-134">Címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhat.</span><span class="sxs-lookup"><span data-stu-id="78f83-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78f83-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="78f83-136">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="78f83-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="78f83-137">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="78f83-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="78f83-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="78f83-139">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="78f83-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="78f83-140">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="78f83-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="78f83-141">-DestinationPortRange</span></span>
<span data-ttu-id="78f83-142">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="78f83-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78f83-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78f83-144">Egész szám</span><span class="sxs-lookup"><span data-stu-id="78f83-144">An integer</span></span>
- <span data-ttu-id="78f83-145">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="78f83-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="78f83-146">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="78f83-146">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-147">-Irány</span><span class="sxs-lookup"><span data-stu-id="78f83-147">-Direction</span></span>
<span data-ttu-id="78f83-148">Azt adja meg, hogy a rendszer kiértékeli-e a szabályt a bejövő vagy kimenő forgalomban.</span><span class="sxs-lookup"><span data-stu-id="78f83-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="78f83-149">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="78f83-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78f83-150">-Name</span></span>
<span data-ttu-id="78f83-151">A hálózati biztonsági szabályok konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-151">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="78f83-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78f83-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="78f83-153">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="78f83-154">Ez a parancsmag hálózati biztonsági szabály konfigurációját adja hozzá az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="78f83-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-155">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="78f83-155">-Priority</span></span>
<span data-ttu-id="78f83-156">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="78f83-157">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="78f83-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="78f83-158">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="78f83-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="78f83-159">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="78f83-159">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-160">-Protocol</span><span class="sxs-lookup"><span data-stu-id="78f83-160">-Protocol</span></span>
<span data-ttu-id="78f83-161">Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="78f83-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="78f83-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78f83-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78f83-163">TCP</span><span class="sxs-lookup"><span data-stu-id="78f83-163">Tcp</span></span>
- <span data-ttu-id="78f83-164">UDP</span><span class="sxs-lookup"><span data-stu-id="78f83-164">Udp</span></span>
- <span data-ttu-id="78f83-165">Helyettesítő karakter (\*) a két érték egyeztetéséhez</span><span class="sxs-lookup"><span data-stu-id="78f83-165">Wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="78f83-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="78f83-167">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="78f83-168">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78f83-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78f83-169">CIDR</span><span class="sxs-lookup"><span data-stu-id="78f83-169">A CIDR</span></span>
- <span data-ttu-id="78f83-170">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="78f83-170">A source IP range</span></span>
- <span data-ttu-id="78f83-171">Egy helyettesítő karakter (\*) az IP-cím megegyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="78f83-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="78f83-172">A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.</span><span class="sxs-lookup"><span data-stu-id="78f83-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78f83-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="78f83-174">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="78f83-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="78f83-175">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="78f83-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="78f83-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="78f83-177">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="78f83-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="78f83-178">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="78f83-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="78f83-179">-SourcePortRange</span></span>
<span data-ttu-id="78f83-180">A forrás-portot vagy-cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f83-180">Specifies a source port or range.</span></span>
<span data-ttu-id="78f83-181">Ezt az értéket egész számként fejezi ki, 0 és 65535 közötti tartománnyal, vagy helyettesítő karakterként (\*), amely a forrás-porthoz igazodik.</span><span class="sxs-lookup"><span data-stu-id="78f83-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f83-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f83-182">CommonParameters</span></span>
<span data-ttu-id="78f83-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78f83-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f83-184">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f83-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f83-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78f83-185">INPUTS</span></span>

### <span data-ttu-id="78f83-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78f83-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="78f83-187">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="78f83-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="78f83-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78f83-188">OUTPUTS</span></span>

### <span data-ttu-id="78f83-189">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78f83-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="78f83-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78f83-190">NOTES</span></span>

## <span data-ttu-id="78f83-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78f83-191">RELATED LINKS</span></span>

[<span data-ttu-id="78f83-192">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78f83-192">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78f83-193">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78f83-193">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78f83-194">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78f83-194">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78f83-195">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78f83-195">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


