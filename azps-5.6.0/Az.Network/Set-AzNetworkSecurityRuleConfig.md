---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003270"
---
# <span data-ttu-id="153eb-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="153eb-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="153eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="153eb-102">SYNOPSIS</span></span>
<span data-ttu-id="153eb-103">Egy hálózati biztonsági csoport hálózati biztonsági szabálykonfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="153eb-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="153eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="153eb-104">SYNTAX</span></span>

### <span data-ttu-id="153eb-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="153eb-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="153eb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="153eb-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="153eb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="153eb-107">DESCRIPTION</span></span>
<span data-ttu-id="153eb-108">A **Set-AzNetworkSecurityRuleConfig** parancsmag frissíti egy hálózati biztonsági szabály konfigurációját egy hálózati biztonsági csoportban.</span><span class="sxs-lookup"><span data-stu-id="153eb-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="153eb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="153eb-109">EXAMPLES</span></span>

### <span data-ttu-id="153eb-110">1. példa: Hozzáférési konfiguráció módosítása hálózati biztonsági szabályban</span><span class="sxs-lookup"><span data-stu-id="153eb-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="153eb-111">Az első parancs leküldi az NSG-FrontEnd nevű hálózati biztonsági csoportot, majd a helyi $nsg.</span><span class="sxs-lookup"><span data-stu-id="153eb-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="153eb-112">A második parancs a folyamatművelettel adja át a biztonsági csoportot a $nsg Get-AzNetworkSecurityRuleConfig szolgáltatásnak, amely megkapja az rdp-rule nevű biztonsági szabály-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="153eb-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="153eb-113">A harmadik parancs az RDP-szabály hozzáférési konfigurációját Elutasításra módosítja.</span><span class="sxs-lookup"><span data-stu-id="153eb-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="153eb-114">Ez azonban felülírja a szabályt, és csak a függvénynek átadott paramétereket Set-AzNetworkSecurityRuleConfig be.</span><span class="sxs-lookup"><span data-stu-id="153eb-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="153eb-115">MEGJEGYZÉS: Egyetlen attribútumot nem lehet módosítani</span><span class="sxs-lookup"><span data-stu-id="153eb-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="153eb-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="153eb-116">Example 2</span></span>

<span data-ttu-id="153eb-117">Egy hálózati biztonsági csoport hálózati biztonsági szabálykonfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="153eb-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="153eb-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="153eb-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="153eb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="153eb-119">PARAMETERS</span></span>

### <span data-ttu-id="153eb-120">-Access</span><span class="sxs-lookup"><span data-stu-id="153eb-120">-Access</span></span>
<span data-ttu-id="153eb-121">Azt adja meg, hogy engedélyezett vagy megtagadható-e a hálózati forgalom.</span><span class="sxs-lookup"><span data-stu-id="153eb-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="153eb-122">A paraméter elfogadható értékei: Allow és Deny.</span><span class="sxs-lookup"><span data-stu-id="153eb-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="153eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153eb-123">-DefaultProfile</span></span>
<span data-ttu-id="153eb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="153eb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="153eb-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="153eb-125">-Description</span></span>
<span data-ttu-id="153eb-126">Megadja a szabálykonfiguráció leírását.</span><span class="sxs-lookup"><span data-stu-id="153eb-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="153eb-127">A maximális méret 140 karakter.</span><span class="sxs-lookup"><span data-stu-id="153eb-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="153eb-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="153eb-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="153eb-129">Megadja a célcím előtagját.</span><span class="sxs-lookup"><span data-stu-id="153eb-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="153eb-130">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="153eb-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="153eb-131">A Classless Interdomain Routing (CIDR) address</span><span class="sxs-lookup"><span data-stu-id="153eb-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="153eb-132">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="153eb-132">A destination IP address range</span></span> 
- <span data-ttu-id="153eb-133">Helyettesítő karakter (\*) bármely IP-címhez. Használhat például VirtualNetwork, AzureLoadBalancer és Internet címkéket.</span><span class="sxs-lookup"><span data-stu-id="153eb-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="153eb-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="153eb-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="153eb-135">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="153eb-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="153eb-136">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="153eb-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="153eb-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="153eb-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="153eb-138">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="153eb-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="153eb-139">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="153eb-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="153eb-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="153eb-140">-DestinationPortRange</span></span>
<span data-ttu-id="153eb-141">Célportot vagy tartományt ad meg.</span><span class="sxs-lookup"><span data-stu-id="153eb-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="153eb-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="153eb-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="153eb-143">Egész szám</span><span class="sxs-lookup"><span data-stu-id="153eb-143">An integer</span></span> 
- <span data-ttu-id="153eb-144">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="153eb-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="153eb-145">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="153eb-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="153eb-146">-Irány</span><span class="sxs-lookup"><span data-stu-id="153eb-146">-Direction</span></span>
<span data-ttu-id="153eb-147">Meghatározza, hogy egy szabály kiértékelve legyen-e a bejövő vagy kimenő forgalomra.</span><span class="sxs-lookup"><span data-stu-id="153eb-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="153eb-148">A paraméter elfogadható értékei a következőek: Bejövő és Kimenő.</span><span class="sxs-lookup"><span data-stu-id="153eb-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="153eb-149">-Name</span><span class="sxs-lookup"><span data-stu-id="153eb-149">-Name</span></span>
<span data-ttu-id="153eb-150">A parancsmag által megadott hálózati biztonsági szabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="153eb-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="153eb-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="153eb-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="153eb-152">Megadja azt **a NetworkSecurityGroup-objektumot,** amely a beállítani kívánt hálózati biztonsági szabály-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="153eb-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="153eb-153">-Priority</span><span class="sxs-lookup"><span data-stu-id="153eb-153">-Priority</span></span>
<span data-ttu-id="153eb-154">Meghatározza a szabálykonfiguráció prioritását.</span><span class="sxs-lookup"><span data-stu-id="153eb-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="153eb-155">A paraméter elfogadható értékei: 100 és 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="153eb-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="153eb-156">A prioritásszámnak egyedinek kell lennie a gyűjtemény minden egyes szabályában.</span><span class="sxs-lookup"><span data-stu-id="153eb-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="153eb-157">Minél kisebb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="153eb-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="153eb-158">-Protocol</span><span class="sxs-lookup"><span data-stu-id="153eb-158">-Protocol</span></span>
<span data-ttu-id="153eb-159">Azt a hálózati protokollt adja meg, amelyre a szabálykonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="153eb-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="153eb-160">A paraméter elfogadható értékei: --Tcp</span><span class="sxs-lookup"><span data-stu-id="153eb-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="153eb-161">Udp</span><span class="sxs-lookup"><span data-stu-id="153eb-161">Udp</span></span>
- <span data-ttu-id="153eb-162">Helyettesítő karakter (\*) mindkét karakterhez</span><span class="sxs-lookup"><span data-stu-id="153eb-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="153eb-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="153eb-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="153eb-164">Megadja a forráscím előtagját.</span><span class="sxs-lookup"><span data-stu-id="153eb-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="153eb-165">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="153eb-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="153eb-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="153eb-166">A CIDR</span></span>
- <span data-ttu-id="153eb-167">Forrás IP-tartomány</span><span class="sxs-lookup"><span data-stu-id="153eb-167">A source IP range</span></span>
- <span data-ttu-id="153eb-168">Egy tetszőleges IP-címnek megfelelő helyettesítő karakter (\*). Használhat olyan címkéket is, mint a VirtualNetwork, az AzureLoadBalancer és az Internet.</span><span class="sxs-lookup"><span data-stu-id="153eb-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="153eb-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="153eb-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="153eb-170">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="153eb-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="153eb-171">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="153eb-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="153eb-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="153eb-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="153eb-173">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="153eb-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="153eb-174">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="153eb-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="153eb-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="153eb-175">-SourcePortRange</span></span>
<span data-ttu-id="153eb-176">A forrásportot vagy -tartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="153eb-176">Specifies the source port or range.</span></span>
<span data-ttu-id="153eb-177">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="153eb-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="153eb-178">Egész szám</span><span class="sxs-lookup"><span data-stu-id="153eb-178">An integer</span></span>
- <span data-ttu-id="153eb-179">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="153eb-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="153eb-180">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="153eb-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="153eb-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153eb-181">CommonParameters</span></span>
<span data-ttu-id="153eb-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="153eb-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153eb-183">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="153eb-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153eb-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="153eb-184">INPUTS</span></span>

### <span data-ttu-id="153eb-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="153eb-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="153eb-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="153eb-186">OUTPUTS</span></span>

### <span data-ttu-id="153eb-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="153eb-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="153eb-188">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="153eb-188">NOTES</span></span>

## <span data-ttu-id="153eb-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="153eb-189">RELATED LINKS</span></span>

[<span data-ttu-id="153eb-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="153eb-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="153eb-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="153eb-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="153eb-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="153eb-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="153eb-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="153eb-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


