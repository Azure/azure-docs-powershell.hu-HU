---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 8a1e4cb97f151843f92697a2a230bd2721a56f29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849937"
---
# <span data-ttu-id="0721b-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0721b-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0721b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0721b-102">SYNOPSIS</span></span>
<span data-ttu-id="0721b-103">Egy hálózati biztonsági szabály konfigurációjának cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="0721b-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0721b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0721b-104">SYNTAX</span></span>

### <span data-ttu-id="0721b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0721b-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="0721b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0721b-106">SetByResourceId</span></span>
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

## <span data-ttu-id="0721b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0721b-107">DESCRIPTION</span></span>
<span data-ttu-id="0721b-108">A **set-AzureRmNetworkSecurityRuleConfig** parancsmag az Azure hálózati biztonsági szabályok konfigurációjának cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="0721b-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="0721b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0721b-109">EXAMPLES</span></span>

### <span data-ttu-id="0721b-110">Példa 1: az Access-konfiguráció módosítása hálózati biztonsági szabályokban</span><span class="sxs-lookup"><span data-stu-id="0721b-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="0721b-111">Az első parancs a NSG-FrontEnd nevű hálózati biztonsági csoportot kapja meg, majd az $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0721b-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="0721b-112">A második parancs a pipeline operátor segítségével továbbítja a biztonsági $nsg csoportot a Get-AzureRmNetworkSecurityRuleConfig, amely az RDP-Rule nevű biztonsági szabály konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="0721b-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="0721b-113">A harmadik parancs az RDP-Rule hozzáférési konfigurációját a Megtagadás értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="0721b-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="0721b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0721b-114">PARAMETERS</span></span>

### <span data-ttu-id="0721b-115">-Access</span><span class="sxs-lookup"><span data-stu-id="0721b-115">-Access</span></span>
<span data-ttu-id="0721b-116">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="0721b-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="0721b-117">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="0721b-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="0721b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0721b-118">-DefaultProfile</span></span>
<span data-ttu-id="0721b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0721b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0721b-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0721b-120">-Description</span></span>
<span data-ttu-id="0721b-121">A szabályok konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="0721b-122">A maximális méret 140 karakter.</span><span class="sxs-lookup"><span data-stu-id="0721b-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="0721b-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0721b-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="0721b-124">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="0721b-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0721b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0721b-126">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="0721b-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="0721b-127">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="0721b-127">A destination IP address range</span></span> 
- <span data-ttu-id="0721b-128">Bármely IP-címnek megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="0721b-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="0721b-129">Címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhat.</span><span class="sxs-lookup"><span data-stu-id="0721b-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="0721b-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0721b-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="0721b-131">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="0721b-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0721b-132">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0721b-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0721b-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0721b-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="0721b-134">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="0721b-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0721b-135">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0721b-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0721b-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="0721b-136">-DestinationPortRange</span></span>
<span data-ttu-id="0721b-137">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="0721b-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0721b-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0721b-139">Egész szám</span><span class="sxs-lookup"><span data-stu-id="0721b-139">An integer</span></span> 
- <span data-ttu-id="0721b-140">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="0721b-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0721b-141">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="0721b-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0721b-142">-Irány</span><span class="sxs-lookup"><span data-stu-id="0721b-142">-Direction</span></span>
<span data-ttu-id="0721b-143">Azt adja meg, hogy a rendszer kiértékeli-e a bejövő vagy kimenő forgalom szabályait.</span><span class="sxs-lookup"><span data-stu-id="0721b-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="0721b-144">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="0721b-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="0721b-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0721b-145">-Name</span></span>
<span data-ttu-id="0721b-146">A parancsmag által beállított hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="0721b-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0721b-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0721b-148">Azt a **NetworkSecurityGroup** -objektumot adja meg, amely a beállítani kívánt hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0721b-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="0721b-149">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="0721b-149">-Priority</span></span>
<span data-ttu-id="0721b-150">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="0721b-151">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="0721b-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="0721b-152">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="0721b-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="0721b-153">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="0721b-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="0721b-154">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0721b-154">-Protocol</span></span>
<span data-ttu-id="0721b-155">Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="0721b-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="0721b-156">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0721b-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="0721b-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="0721b-157">--Tcp</span></span>
- <span data-ttu-id="0721b-158">UDP</span><span class="sxs-lookup"><span data-stu-id="0721b-158">Udp</span></span>
- <span data-ttu-id="0721b-159">Helyettesítő karakter (\*) a két érték egyeztetéséhez</span><span class="sxs-lookup"><span data-stu-id="0721b-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="0721b-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0721b-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="0721b-161">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="0721b-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0721b-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0721b-163">CIDR</span><span class="sxs-lookup"><span data-stu-id="0721b-163">A CIDR</span></span>
- <span data-ttu-id="0721b-164">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="0721b-164">A source IP range</span></span>
- <span data-ttu-id="0721b-165">Bármely IP-címnek megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="0721b-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="0721b-166">A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.</span><span class="sxs-lookup"><span data-stu-id="0721b-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="0721b-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0721b-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="0721b-168">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0721b-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="0721b-169">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0721b-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0721b-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0721b-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="0721b-171">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0721b-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="0721b-172">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="0721b-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0721b-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="0721b-173">-SourcePortRange</span></span>
<span data-ttu-id="0721b-174">A forrás portját vagy a tartománnyal adja meg.</span><span class="sxs-lookup"><span data-stu-id="0721b-174">Specifies the source port or range.</span></span>
<span data-ttu-id="0721b-175">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0721b-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0721b-176">Egész szám</span><span class="sxs-lookup"><span data-stu-id="0721b-176">An integer</span></span>
- <span data-ttu-id="0721b-177">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="0721b-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0721b-178">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="0721b-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0721b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0721b-179">CommonParameters</span></span>
<span data-ttu-id="0721b-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0721b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0721b-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0721b-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0721b-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0721b-182">INPUTS</span></span>

### <span data-ttu-id="0721b-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0721b-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0721b-184">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0721b-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="0721b-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0721b-185">OUTPUTS</span></span>

### <span data-ttu-id="0721b-186">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0721b-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0721b-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0721b-187">NOTES</span></span>

## <span data-ttu-id="0721b-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0721b-188">RELATED LINKS</span></span>

[<span data-ttu-id="0721b-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0721b-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0721b-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0721b-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0721b-191">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0721b-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0721b-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0721b-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


