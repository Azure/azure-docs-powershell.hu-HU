---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: e30a03f82d0bcf719ffc4dc5640e3fbf9b3bb99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501728"
---
# <span data-ttu-id="9f18f-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f18f-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9f18f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f18f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f18f-103">Hálózati biztonsági szabály konfigurációjának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9f18f-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f18f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f18f-104">SYNTAX</span></span>

### <span data-ttu-id="9f18f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f18f-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f18f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f18f-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f18f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f18f-107">DESCRIPTION</span></span>
<span data-ttu-id="9f18f-108">A **New-AzureRmNetworkSecurityRuleConfig** parancsmag az Azure hálózat biztonsági szabályának konfigurációját hozza létre egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="9f18f-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="9f18f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f18f-109">EXAMPLES</span></span>

### <span data-ttu-id="9f18f-110">1: hálózati biztonsági szabály létrehozása az RDP protokoll engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="9f18f-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="9f18f-111">Ez a parancs létrehoz egy biztonsági szabályt, amely lehetővé teszi az internetről a 3389-as port elérését</span><span class="sxs-lookup"><span data-stu-id="9f18f-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="9f18f-112">2: hálózati biztonsági szabály létrehozása, amely lehetővé teszi a HTTP-t</span><span class="sxs-lookup"><span data-stu-id="9f18f-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="9f18f-113">Ez a parancs létrehoz egy biztonsági szabályt, amely lehetővé teszi az internetről a 80-as port elérését</span><span class="sxs-lookup"><span data-stu-id="9f18f-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="9f18f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f18f-114">PARAMETERS</span></span>

### <span data-ttu-id="9f18f-115">-Access</span><span class="sxs-lookup"><span data-stu-id="9f18f-115">-Access</span></span>
<span data-ttu-id="9f18f-116">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="9f18f-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="9f18f-117">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="9f18f-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="9f18f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f18f-118">-DefaultProfile</span></span>
<span data-ttu-id="9f18f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f18f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f18f-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9f18f-120">-Description</span></span>
<span data-ttu-id="9f18f-121">A létrehozandó hálózati biztonsági szabály konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="9f18f-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9f18f-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="9f18f-123">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="9f18f-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f18f-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f18f-125">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="9f18f-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="9f18f-126">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="9f18f-126">A destination IP address range</span></span> 
- <span data-ttu-id="9f18f-127">Bármely IP-címnek megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="9f18f-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="9f18f-128">Címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhat.</span><span class="sxs-lookup"><span data-stu-id="9f18f-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="9f18f-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f18f-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="9f18f-130">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="9f18f-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9f18f-131">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="9f18f-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9f18f-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9f18f-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="9f18f-133">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="9f18f-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9f18f-134">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="9f18f-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9f18f-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="9f18f-135">-DestinationPortRange</span></span>
<span data-ttu-id="9f18f-136">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="9f18f-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f18f-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f18f-138">Egész szám</span><span class="sxs-lookup"><span data-stu-id="9f18f-138">An integer</span></span>
- <span data-ttu-id="9f18f-139">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="9f18f-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9f18f-140">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="9f18f-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9f18f-141">-Irány</span><span class="sxs-lookup"><span data-stu-id="9f18f-141">-Direction</span></span>
<span data-ttu-id="9f18f-142">Azt adja meg, hogy a rendszer kiértékeli-e a szabályt a bejövő vagy kimenő forgalomban.</span><span class="sxs-lookup"><span data-stu-id="9f18f-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="9f18f-143">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="9f18f-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="9f18f-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f18f-144">-Name</span></span>
<span data-ttu-id="9f18f-145">A parancsmag által létrehozott hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9f18f-146">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="9f18f-146">-Priority</span></span>
<span data-ttu-id="9f18f-147">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="9f18f-148">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="9f18f-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="9f18f-149">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="9f18f-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="9f18f-150">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="9f18f-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="9f18f-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9f18f-151">-Protocol</span></span>
<span data-ttu-id="9f18f-152">Azt a hálózati protokollt adja meg, amelyre az új szabály-konfiguráció vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="9f18f-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="9f18f-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f18f-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f18f-154">TCP</span><span class="sxs-lookup"><span data-stu-id="9f18f-154">Tcp</span></span>
- <span data-ttu-id="9f18f-155">UDP</span><span class="sxs-lookup"><span data-stu-id="9f18f-155">Udp</span></span>
- <span data-ttu-id="9f18f-156">a helyettesítő karakter (\*) a két érték egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="9f18f-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="9f18f-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9f18f-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="9f18f-158">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="9f18f-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f18f-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f18f-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="9f18f-160">A CIDR</span></span>
- <span data-ttu-id="9f18f-161">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="9f18f-161">A source IP range</span></span>
- <span data-ttu-id="9f18f-162">Egy helyettesítő karakter (\*) az IP-cím megegyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="9f18f-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="9f18f-163">A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.</span><span class="sxs-lookup"><span data-stu-id="9f18f-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="9f18f-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f18f-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="9f18f-165">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="9f18f-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="9f18f-166">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="9f18f-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9f18f-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9f18f-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="9f18f-168">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="9f18f-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="9f18f-169">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="9f18f-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9f18f-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="9f18f-170">-SourcePortRange</span></span>
<span data-ttu-id="9f18f-171">A forrás portját vagy a tartománnyal adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f18f-171">Specifies the source port or range.</span></span>
<span data-ttu-id="9f18f-172">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f18f-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f18f-173">Egész szám</span><span class="sxs-lookup"><span data-stu-id="9f18f-173">An integer</span></span>
- <span data-ttu-id="9f18f-174">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="9f18f-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9f18f-175">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="9f18f-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9f18f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f18f-176">CommonParameters</span></span>
<span data-ttu-id="9f18f-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f18f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f18f-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f18f-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f18f-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f18f-179">INPUTS</span></span>

## <span data-ttu-id="9f18f-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f18f-180">OUTPUTS</span></span>

### <span data-ttu-id="9f18f-181">Microsoft. Azure. commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9f18f-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="9f18f-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f18f-182">NOTES</span></span>

## <span data-ttu-id="9f18f-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f18f-183">RELATED LINKS</span></span>

[<span data-ttu-id="9f18f-184">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f18f-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9f18f-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f18f-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9f18f-186">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f18f-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9f18f-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f18f-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

