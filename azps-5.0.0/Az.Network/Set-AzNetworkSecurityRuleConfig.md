---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186736"
---
# <span data-ttu-id="17083-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17083-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="17083-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17083-102">SYNOPSIS</span></span>
<span data-ttu-id="17083-103">Egy hálózati biztonsági szabály konfigurációjának frissítése egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="17083-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="17083-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17083-104">SYNTAX</span></span>

### <span data-ttu-id="17083-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17083-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17083-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="17083-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17083-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="17083-107">DESCRIPTION</span></span>
<span data-ttu-id="17083-108">A **set-AzNetworkSecurityRuleConfig** parancsmag egy hálózati biztonsági szabály konfigurációját frissíti egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="17083-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="17083-109">Példák</span><span class="sxs-lookup"><span data-stu-id="17083-109">EXAMPLES</span></span>

### <span data-ttu-id="17083-110">Példa 1: az Access-konfiguráció módosítása hálózati biztonsági szabályokban</span><span class="sxs-lookup"><span data-stu-id="17083-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="17083-111">Az első parancs a NSG-FrontEnd nevű hálózati biztonsági csoportot kapja meg, majd az $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="17083-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="17083-112">A második parancs a pipeline operátor segítségével továbbítja a biztonsági $nsg csoportot a Get-AzNetworkSecurityRuleConfig, amely az RDP-Rule nevű biztonsági szabály konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="17083-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="17083-113">A harmadik parancs az RDP-Rule hozzáférési konfigurációját a Megtagadás értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="17083-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="17083-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="17083-114">Example 2</span></span>

<span data-ttu-id="17083-115">Egy hálózati biztonsági szabály konfigurációjának frissítése egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="17083-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="17083-116">autogenerated</span><span class="sxs-lookup"><span data-stu-id="17083-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="17083-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17083-117">PARAMETERS</span></span>

### <span data-ttu-id="17083-118">-Access</span><span class="sxs-lookup"><span data-stu-id="17083-118">-Access</span></span>
<span data-ttu-id="17083-119">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="17083-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="17083-120">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="17083-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="17083-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17083-121">-DefaultProfile</span></span>
<span data-ttu-id="17083-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17083-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17083-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="17083-123">-Description</span></span>
<span data-ttu-id="17083-124">A szabályok konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="17083-125">A maximális méret 140 karakter.</span><span class="sxs-lookup"><span data-stu-id="17083-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="17083-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="17083-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="17083-127">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="17083-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="17083-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17083-129">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="17083-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="17083-130">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="17083-130">A destination IP address range</span></span> 
- <span data-ttu-id="17083-131">A helyettesítő karakter (\*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.</span><span class="sxs-lookup"><span data-stu-id="17083-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="17083-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="17083-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="17083-133">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="17083-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="17083-134">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="17083-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="17083-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="17083-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="17083-136">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="17083-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="17083-137">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="17083-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="17083-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="17083-138">-DestinationPortRange</span></span>
<span data-ttu-id="17083-139">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="17083-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="17083-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17083-141">Egész szám</span><span class="sxs-lookup"><span data-stu-id="17083-141">An integer</span></span> 
- <span data-ttu-id="17083-142">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="17083-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="17083-143">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="17083-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="17083-144">-Irány</span><span class="sxs-lookup"><span data-stu-id="17083-144">-Direction</span></span>
<span data-ttu-id="17083-145">Azt adja meg, hogy a rendszer kiértékeli-e a bejövő vagy kimenő forgalom szabályait.</span><span class="sxs-lookup"><span data-stu-id="17083-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="17083-146">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="17083-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="17083-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17083-147">-Name</span></span>
<span data-ttu-id="17083-148">A parancsmag által beállított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="17083-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="17083-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="17083-150">Azt a **NetworkSecurityGroup** -objektumot adja meg, amely a beállítani kívánt hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="17083-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="17083-151">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="17083-151">-Priority</span></span>
<span data-ttu-id="17083-152">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="17083-153">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="17083-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="17083-154">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="17083-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="17083-155">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="17083-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="17083-156">-Protocol</span><span class="sxs-lookup"><span data-stu-id="17083-156">-Protocol</span></span>
<span data-ttu-id="17083-157">Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="17083-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="17083-158">A paraméter elfogadható értékei a következők:--– TCP</span><span class="sxs-lookup"><span data-stu-id="17083-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="17083-159">UDP</span><span class="sxs-lookup"><span data-stu-id="17083-159">Udp</span></span>
- <span data-ttu-id="17083-160">Helyettesítő karakter (\*) a két érték egyeztetéséhez</span><span class="sxs-lookup"><span data-stu-id="17083-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="17083-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="17083-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="17083-162">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="17083-163">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="17083-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17083-164">CIDR</span><span class="sxs-lookup"><span data-stu-id="17083-164">A CIDR</span></span>
- <span data-ttu-id="17083-165">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="17083-165">A source IP range</span></span>
- <span data-ttu-id="17083-166">A helyettesítő karakter (\*) bármely IP-címhez való egyezéshez használhatja a címkéket, például a VirtualNetwork, az AzureLoadBalancer és az internetet is.</span><span class="sxs-lookup"><span data-stu-id="17083-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="17083-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="17083-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="17083-168">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="17083-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="17083-169">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="17083-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="17083-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="17083-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="17083-171">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="17083-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="17083-172">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="17083-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="17083-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="17083-173">-SourcePortRange</span></span>
<span data-ttu-id="17083-174">A forrás portját vagy a tartománnyal adja meg.</span><span class="sxs-lookup"><span data-stu-id="17083-174">Specifies the source port or range.</span></span>
<span data-ttu-id="17083-175">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="17083-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17083-176">Egész szám</span><span class="sxs-lookup"><span data-stu-id="17083-176">An integer</span></span>
- <span data-ttu-id="17083-177">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="17083-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="17083-178">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="17083-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="17083-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17083-179">CommonParameters</span></span>
<span data-ttu-id="17083-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17083-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17083-181">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17083-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17083-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17083-182">INPUTS</span></span>

### <span data-ttu-id="17083-183">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="17083-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="17083-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17083-184">OUTPUTS</span></span>

### <span data-ttu-id="17083-185">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="17083-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="17083-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17083-186">NOTES</span></span>

## <span data-ttu-id="17083-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17083-187">RELATED LINKS</span></span>

[<span data-ttu-id="17083-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17083-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="17083-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17083-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="17083-190">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17083-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="17083-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17083-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


