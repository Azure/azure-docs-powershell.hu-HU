---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: cff46867b92010969118ced67f53f5bd94c8337f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012483"
---
# <span data-ttu-id="e66d1-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e66d1-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e66d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e66d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e66d1-103">Egy hálózati biztonsági szabály konfigurációjának frissítése egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="e66d1-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="e66d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e66d1-104">SYNTAX</span></span>

### <span data-ttu-id="e66d1-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e66d1-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e66d1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e66d1-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e66d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e66d1-107">DESCRIPTION</span></span>
<span data-ttu-id="e66d1-108">A **set-AzNetworkSecurityRuleConfig** parancsmag egy hálózati biztonsági szabály konfigurációját frissíti egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="e66d1-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="e66d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e66d1-109">EXAMPLES</span></span>

### <span data-ttu-id="e66d1-110">Példa 1: az Access-konfiguráció módosítása hálózati biztonsági szabályokban</span><span class="sxs-lookup"><span data-stu-id="e66d1-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="e66d1-111">Az első parancs a NSG-FrontEnd nevű hálózati biztonsági csoportot kapja meg, majd az $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e66d1-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="e66d1-112">A második parancs a pipeline operátor segítségével továbbítja a biztonsági $nsg csoportot a Get-AzNetworkSecurityRuleConfig, amely az RDP-Rule nevű biztonsági szabály konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="e66d1-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="e66d1-113">A harmadik parancs az RDP-Rule hozzáférési konfigurációját a Megtagadás értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="e66d1-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="e66d1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e66d1-114">PARAMETERS</span></span>

### <span data-ttu-id="e66d1-115">-Access</span><span class="sxs-lookup"><span data-stu-id="e66d1-115">-Access</span></span>
<span data-ttu-id="e66d1-116">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="e66d1-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="e66d1-117">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="e66d1-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="e66d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e66d1-118">-DefaultProfile</span></span>
<span data-ttu-id="e66d1-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e66d1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e66d1-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e66d1-120">-Description</span></span>
<span data-ttu-id="e66d1-121">A szabályok konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="e66d1-122">A maximális méret 140 karakter.</span><span class="sxs-lookup"><span data-stu-id="e66d1-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="e66d1-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e66d1-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="e66d1-124">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="e66d1-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e66d1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e66d1-126">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="e66d1-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="e66d1-127">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="e66d1-127">A destination IP address range</span></span> 
- <span data-ttu-id="e66d1-128">A helyettesítő karakter (\*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.</span><span class="sxs-lookup"><span data-stu-id="e66d1-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="e66d1-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e66d1-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="e66d1-130">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="e66d1-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="e66d1-131">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="e66d1-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="e66d1-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e66d1-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="e66d1-133">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="e66d1-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="e66d1-134">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="e66d1-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="e66d1-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="e66d1-135">-DestinationPortRange</span></span>
<span data-ttu-id="e66d1-136">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="e66d1-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e66d1-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e66d1-138">Egész szám</span><span class="sxs-lookup"><span data-stu-id="e66d1-138">An integer</span></span> 
- <span data-ttu-id="e66d1-139">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="e66d1-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="e66d1-140">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="e66d1-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="e66d1-141">-Irány</span><span class="sxs-lookup"><span data-stu-id="e66d1-141">-Direction</span></span>
<span data-ttu-id="e66d1-142">Azt adja meg, hogy a rendszer kiértékeli-e a bejövő vagy kimenő forgalom szabályait.</span><span class="sxs-lookup"><span data-stu-id="e66d1-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="e66d1-143">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="e66d1-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="e66d1-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e66d1-144">-Name</span></span>
<span data-ttu-id="e66d1-145">A parancsmag által beállított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="e66d1-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e66d1-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e66d1-147">Azt a **NetworkSecurityGroup** -objektumot adja meg, amely a beállítani kívánt hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e66d1-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="e66d1-148">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="e66d1-148">-Priority</span></span>
<span data-ttu-id="e66d1-149">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="e66d1-150">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="e66d1-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="e66d1-151">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="e66d1-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="e66d1-152">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="e66d1-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="e66d1-153">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e66d1-153">-Protocol</span></span>
<span data-ttu-id="e66d1-154">Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e66d1-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="e66d1-155">A paraméter elfogadható értékei a következők:--– TCP</span><span class="sxs-lookup"><span data-stu-id="e66d1-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="e66d1-156">UDP</span><span class="sxs-lookup"><span data-stu-id="e66d1-156">Udp</span></span>
- <span data-ttu-id="e66d1-157">Helyettesítő karakter (\*) a két érték egyeztetéséhez</span><span class="sxs-lookup"><span data-stu-id="e66d1-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="e66d1-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e66d1-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="e66d1-159">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="e66d1-160">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e66d1-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e66d1-161">CIDR</span><span class="sxs-lookup"><span data-stu-id="e66d1-161">A CIDR</span></span>
- <span data-ttu-id="e66d1-162">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="e66d1-162">A source IP range</span></span>
- <span data-ttu-id="e66d1-163">A helyettesítő karakter (\*) bármely IP-címhez való egyezéshez használhatja a címkéket, például a VirtualNetwork, az AzureLoadBalancer és az internetet is.</span><span class="sxs-lookup"><span data-stu-id="e66d1-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="e66d1-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e66d1-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="e66d1-165">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="e66d1-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="e66d1-166">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="e66d1-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="e66d1-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e66d1-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="e66d1-168">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="e66d1-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="e66d1-169">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="e66d1-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="e66d1-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="e66d1-170">-SourcePortRange</span></span>
<span data-ttu-id="e66d1-171">A forrás portját vagy a tartománnyal adja meg.</span><span class="sxs-lookup"><span data-stu-id="e66d1-171">Specifies the source port or range.</span></span>
<span data-ttu-id="e66d1-172">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e66d1-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e66d1-173">Egész szám</span><span class="sxs-lookup"><span data-stu-id="e66d1-173">An integer</span></span>
- <span data-ttu-id="e66d1-174">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="e66d1-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="e66d1-175">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="e66d1-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="e66d1-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66d1-176">CommonParameters</span></span>
<span data-ttu-id="e66d1-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e66d1-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66d1-178">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e66d1-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66d1-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e66d1-179">INPUTS</span></span>

### <span data-ttu-id="e66d1-180">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e66d1-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e66d1-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e66d1-181">OUTPUTS</span></span>

### <span data-ttu-id="e66d1-182">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e66d1-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e66d1-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e66d1-183">NOTES</span></span>

## <span data-ttu-id="e66d1-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e66d1-184">RELATED LINKS</span></span>

[<span data-ttu-id="e66d1-185">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e66d1-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e66d1-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e66d1-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e66d1-187">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e66d1-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e66d1-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e66d1-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


