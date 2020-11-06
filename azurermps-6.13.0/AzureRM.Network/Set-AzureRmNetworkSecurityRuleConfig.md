---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: f9c0e2b2071bdcae348d6bbd5237a355601e9fad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494997"
---
# <span data-ttu-id="0292e-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0292e-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0292e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0292e-102">SYNOPSIS</span></span>
<span data-ttu-id="0292e-103">Egy hálózati biztonsági szabály konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="0292e-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0292e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0292e-104">SYNTAX</span></span>

### <span data-ttu-id="0292e-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0292e-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="0292e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0292e-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0292e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0292e-107">DESCRIPTION</span></span>
<span data-ttu-id="0292e-108">A **set-AzureRmNetworkSecurityRuleConfig** parancsmag az Azure hálózati biztonsági szabályok konfigurációjának cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="0292e-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="0292e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0292e-109">EXAMPLES</span></span>

### <span data-ttu-id="0292e-110">Példa 1: az Access-konfiguráció módosítása hálózati biztonsági szabályokban</span><span class="sxs-lookup"><span data-stu-id="0292e-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="0292e-111">Az első parancs a NSG-FrontEnd nevű hálózati biztonsági csoportot kapja meg, majd az $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0292e-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="0292e-112">A második parancs a pipeline operátor segítségével továbbítja a biztonsági $nsg csoportot a Get-AzureRmNetworkSecurityRuleConfig, amely az RDP-Rule nevű biztonsági szabály konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="0292e-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="0292e-113">A harmadik parancs az RDP-Rule hozzáférési konfigurációját a Megtagadás értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="0292e-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="0292e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0292e-114">PARAMETERS</span></span>

### <span data-ttu-id="0292e-115">-Access</span><span class="sxs-lookup"><span data-stu-id="0292e-115">-Access</span></span>
<span data-ttu-id="0292e-116">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="0292e-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="0292e-117">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="0292e-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="0292e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0292e-118">-DefaultProfile</span></span>
<span data-ttu-id="0292e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0292e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0292e-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0292e-120">-Description</span></span>
<span data-ttu-id="0292e-121">A szabályok konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="0292e-122">A maximális méret 140 karakter.</span><span class="sxs-lookup"><span data-stu-id="0292e-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="0292e-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0292e-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="0292e-124">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="0292e-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0292e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0292e-126">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="0292e-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="0292e-127">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="0292e-127">A destination IP address range</span></span> 
- <span data-ttu-id="0292e-128">A helyettesítő karakter (\*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.</span><span class="sxs-lookup"><span data-stu-id="0292e-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="0292e-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0292e-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="0292e-130">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="0292e-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0292e-131">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0292e-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0292e-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0292e-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="0292e-133">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="0292e-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0292e-134">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0292e-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0292e-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="0292e-135">-DestinationPortRange</span></span>
<span data-ttu-id="0292e-136">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="0292e-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0292e-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0292e-138">Egész szám</span><span class="sxs-lookup"><span data-stu-id="0292e-138">An integer</span></span> 
- <span data-ttu-id="0292e-139">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="0292e-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0292e-140">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="0292e-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0292e-141">-Irány</span><span class="sxs-lookup"><span data-stu-id="0292e-141">-Direction</span></span>
<span data-ttu-id="0292e-142">Azt adja meg, hogy a rendszer kiértékeli-e a bejövő vagy kimenő forgalom szabályait.</span><span class="sxs-lookup"><span data-stu-id="0292e-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="0292e-143">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="0292e-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="0292e-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0292e-144">-Name</span></span>
<span data-ttu-id="0292e-145">A parancsmag által beállított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="0292e-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0292e-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0292e-147">Azt a **NetworkSecurityGroup** -objektumot adja meg, amely a beállítani kívánt hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0292e-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="0292e-148">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="0292e-148">-Priority</span></span>
<span data-ttu-id="0292e-149">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="0292e-150">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="0292e-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="0292e-151">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="0292e-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="0292e-152">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="0292e-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="0292e-153">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0292e-153">-Protocol</span></span>
<span data-ttu-id="0292e-154">Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="0292e-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="0292e-155">A paraméter elfogadható értékei a következők:--– TCP</span><span class="sxs-lookup"><span data-stu-id="0292e-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="0292e-156">UDP</span><span class="sxs-lookup"><span data-stu-id="0292e-156">Udp</span></span>
- <span data-ttu-id="0292e-157">Helyettesítő karakter (\*) a két érték egyeztetéséhez</span><span class="sxs-lookup"><span data-stu-id="0292e-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="0292e-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0292e-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="0292e-159">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="0292e-160">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0292e-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0292e-161">CIDR</span><span class="sxs-lookup"><span data-stu-id="0292e-161">A CIDR</span></span>
- <span data-ttu-id="0292e-162">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="0292e-162">A source IP range</span></span>
- <span data-ttu-id="0292e-163">A helyettesítő karakter (\*) bármely IP-címhez való egyezéshez használhatja a címkéket, például a VirtualNetwork, az AzureLoadBalancer és az internetet is.</span><span class="sxs-lookup"><span data-stu-id="0292e-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="0292e-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0292e-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="0292e-165">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0292e-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="0292e-166">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0292e-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0292e-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0292e-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="0292e-168">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0292e-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="0292e-169">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0292e-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0292e-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="0292e-170">-SourcePortRange</span></span>
<span data-ttu-id="0292e-171">A forrás portját vagy a tartománnyal adja meg.</span><span class="sxs-lookup"><span data-stu-id="0292e-171">Specifies the source port or range.</span></span>
<span data-ttu-id="0292e-172">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0292e-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0292e-173">Egész szám</span><span class="sxs-lookup"><span data-stu-id="0292e-173">An integer</span></span>
- <span data-ttu-id="0292e-174">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="0292e-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0292e-175">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="0292e-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0292e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0292e-176">CommonParameters</span></span>
<span data-ttu-id="0292e-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0292e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0292e-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0292e-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0292e-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0292e-179">INPUTS</span></span>

### <span data-ttu-id="0292e-180">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0292e-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0292e-181">Paraméterek: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0292e-181">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="0292e-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0292e-182">OUTPUTS</span></span>

### <span data-ttu-id="0292e-183">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0292e-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0292e-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0292e-184">NOTES</span></span>

## <span data-ttu-id="0292e-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0292e-185">RELATED LINKS</span></span>

[<span data-ttu-id="0292e-186">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0292e-186">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0292e-187">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0292e-187">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0292e-188">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0292e-188">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0292e-189">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0292e-189">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


