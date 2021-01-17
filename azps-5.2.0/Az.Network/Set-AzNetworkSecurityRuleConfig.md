---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371572"
---
# <span data-ttu-id="5a77c-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a77c-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="5a77c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a77c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a77c-103">Egy hálózati biztonsági csoport hálózati biztonsági szabálykonfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="5a77c-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5a77c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a77c-104">SYNTAX</span></span>

### <span data-ttu-id="5a77c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a77c-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a77c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a77c-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a77c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a77c-107">DESCRIPTION</span></span>
<span data-ttu-id="5a77c-108">A **Set-AzNetworkSecurityRuleConfig** parancsmag frissíti egy hálózati biztonsági szabály konfigurációját egy hálózati biztonsági csoportban.</span><span class="sxs-lookup"><span data-stu-id="5a77c-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5a77c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a77c-109">EXAMPLES</span></span>

### <span data-ttu-id="5a77c-110">1. példa: Hozzáférési konfiguráció módosítása hálózati biztonsági szabályban</span><span class="sxs-lookup"><span data-stu-id="5a77c-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="5a77c-111">Az első parancs leküldi az NSG-FrontEnd nevű hálózati biztonsági csoportot, majd a helyi $nsg.</span><span class="sxs-lookup"><span data-stu-id="5a77c-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="5a77c-112">A második parancs a folyamatművelettel adja át a biztonsági csoportot a $nsg-AzNetworkSecurityRuleConfig szolgáltatásnak, amely az rdp-rule nevű biztonsági szabály-konfigurációt kapja.</span><span class="sxs-lookup"><span data-stu-id="5a77c-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="5a77c-113">A harmadik parancs az RDP-szabály hozzáférési konfigurációját Elutasításra módosítja.</span><span class="sxs-lookup"><span data-stu-id="5a77c-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="5a77c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5a77c-114">Example 2</span></span>

<span data-ttu-id="5a77c-115">Egy hálózati biztonsági csoport hálózati biztonsági szabálykonfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="5a77c-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="5a77c-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="5a77c-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="5a77c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a77c-117">PARAMETERS</span></span>

### <span data-ttu-id="5a77c-118">-Access</span><span class="sxs-lookup"><span data-stu-id="5a77c-118">-Access</span></span>
<span data-ttu-id="5a77c-119">Azt adja meg, hogy engedélyezett vagy megtagadható-e a hálózati forgalom.</span><span class="sxs-lookup"><span data-stu-id="5a77c-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="5a77c-120">A paraméter elfogadható értékei: Allow és Deny.</span><span class="sxs-lookup"><span data-stu-id="5a77c-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="5a77c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a77c-121">-DefaultProfile</span></span>
<span data-ttu-id="5a77c-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a77c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a77c-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5a77c-123">-Description</span></span>
<span data-ttu-id="5a77c-124">Megadja a szabálykonfiguráció leírását.</span><span class="sxs-lookup"><span data-stu-id="5a77c-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="5a77c-125">A maximális méret 140 karakter.</span><span class="sxs-lookup"><span data-stu-id="5a77c-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="5a77c-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5a77c-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="5a77c-127">Megadja a célcím előtagját.</span><span class="sxs-lookup"><span data-stu-id="5a77c-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="5a77c-128">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5a77c-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a77c-129">A Classless Interdomain Routing (CIDR) address</span><span class="sxs-lookup"><span data-stu-id="5a77c-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="5a77c-130">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="5a77c-130">A destination IP address range</span></span> 
- <span data-ttu-id="5a77c-131">Helyettesítő karakter (\*) bármely IP-címhez. Használhat például VirtualNetwork, AzureLoadBalancer és Internet címkéket.</span><span class="sxs-lookup"><span data-stu-id="5a77c-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="5a77c-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a77c-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="5a77c-133">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="5a77c-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="5a77c-134">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="5a77c-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5a77c-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5a77c-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="5a77c-136">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="5a77c-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="5a77c-137">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="5a77c-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5a77c-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="5a77c-138">-DestinationPortRange</span></span>
<span data-ttu-id="5a77c-139">Célportot vagy tartományt ad meg.</span><span class="sxs-lookup"><span data-stu-id="5a77c-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="5a77c-140">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5a77c-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a77c-141">Egész szám</span><span class="sxs-lookup"><span data-stu-id="5a77c-141">An integer</span></span> 
- <span data-ttu-id="5a77c-142">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="5a77c-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="5a77c-143">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="5a77c-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="5a77c-144">-Irány</span><span class="sxs-lookup"><span data-stu-id="5a77c-144">-Direction</span></span>
<span data-ttu-id="5a77c-145">Meghatározza, hogy egy szabály kiértékelve legyen-e a bejövő vagy kimenő forgalomra.</span><span class="sxs-lookup"><span data-stu-id="5a77c-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="5a77c-146">A paraméter elfogadható értékei a következőek: Bejövő és Kimenő.</span><span class="sxs-lookup"><span data-stu-id="5a77c-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="5a77c-147">-Name</span><span class="sxs-lookup"><span data-stu-id="5a77c-147">-Name</span></span>
<span data-ttu-id="5a77c-148">A parancsmag által megadott hálózati biztonsági szabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a77c-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="5a77c-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a77c-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5a77c-150">Azt a **NetworkSecurityGroup-objektumot** adja meg, amely a beállítani kívánt hálózati biztonsági szabály-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5a77c-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="5a77c-151">-Priority</span><span class="sxs-lookup"><span data-stu-id="5a77c-151">-Priority</span></span>
<span data-ttu-id="5a77c-152">Meghatározza a szabálykonfiguráció prioritását.</span><span class="sxs-lookup"><span data-stu-id="5a77c-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="5a77c-153">A paraméter elfogadható értékei: 100 és 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="5a77c-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="5a77c-154">A prioritásszámnak egyedinek kell lennie a gyűjtemény minden egyes szabályában.</span><span class="sxs-lookup"><span data-stu-id="5a77c-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="5a77c-155">Minél kisebb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="5a77c-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="5a77c-156">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5a77c-156">-Protocol</span></span>
<span data-ttu-id="5a77c-157">Azt a hálózati protokollt adja meg, amelyre a szabálykonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="5a77c-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="5a77c-158">A paraméter elfogadható értékei: --Tcp</span><span class="sxs-lookup"><span data-stu-id="5a77c-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="5a77c-159">Udp</span><span class="sxs-lookup"><span data-stu-id="5a77c-159">Udp</span></span>
- <span data-ttu-id="5a77c-160">Helyettesítő karakter (\*) mindkét karakterhez</span><span class="sxs-lookup"><span data-stu-id="5a77c-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="5a77c-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5a77c-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="5a77c-162">Megadja a forráscím előtagját.</span><span class="sxs-lookup"><span data-stu-id="5a77c-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="5a77c-163">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5a77c-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a77c-164">A CIDR</span><span class="sxs-lookup"><span data-stu-id="5a77c-164">A CIDR</span></span>
- <span data-ttu-id="5a77c-165">Forrás IP-tartomány</span><span class="sxs-lookup"><span data-stu-id="5a77c-165">A source IP range</span></span>
- <span data-ttu-id="5a77c-166">Egy tetszőleges IP-címnek megfelelő helyettesítő karakter (\*). Használhat olyan címkéket is, mint a VirtualNetwork, az AzureLoadBalancer és az Internet.</span><span class="sxs-lookup"><span data-stu-id="5a77c-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="5a77c-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a77c-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="5a77c-168">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="5a77c-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="5a77c-169">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="5a77c-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5a77c-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5a77c-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="5a77c-171">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="5a77c-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="5a77c-172">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="5a77c-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5a77c-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="5a77c-173">-SourcePortRange</span></span>
<span data-ttu-id="5a77c-174">A forrásportot vagy -tartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a77c-174">Specifies the source port or range.</span></span>
<span data-ttu-id="5a77c-175">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5a77c-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a77c-176">Egész szám</span><span class="sxs-lookup"><span data-stu-id="5a77c-176">An integer</span></span>
- <span data-ttu-id="5a77c-177">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="5a77c-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="5a77c-178">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="5a77c-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="5a77c-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a77c-179">CommonParameters</span></span>
<span data-ttu-id="5a77c-180">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a77c-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a77c-181">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a77c-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a77c-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a77c-182">INPUTS</span></span>

### <span data-ttu-id="5a77c-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a77c-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a77c-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a77c-184">OUTPUTS</span></span>

### <span data-ttu-id="5a77c-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a77c-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a77c-186">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a77c-186">NOTES</span></span>

## <span data-ttu-id="5a77c-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a77c-187">RELATED LINKS</span></span>

[<span data-ttu-id="5a77c-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a77c-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5a77c-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a77c-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5a77c-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a77c-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5a77c-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a77c-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


