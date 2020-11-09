---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301478"
---
# <span data-ttu-id="7f89c-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f89c-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7f89c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f89c-103">Hálózati biztonsági szabály konfigurációjának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="7f89c-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="7f89c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f89c-104">SYNTAX</span></span>

### <span data-ttu-id="7f89c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f89c-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f89c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f89c-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f89c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f89c-107">DESCRIPTION</span></span>
<span data-ttu-id="7f89c-108">A **New-AzNetworkSecurityRuleConfig** parancsmag az Azure hálózat biztonsági szabályának konfigurációját hozza létre egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="7f89c-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="7f89c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7f89c-109">EXAMPLES</span></span>

### <span data-ttu-id="7f89c-110">Példa 1: hálózati biztonsági szabály létrehozása az RDP protokoll engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="7f89c-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="7f89c-111">Ez a parancs létrehoz egy biztonsági szabályt, amely lehetővé teszi az internetről a 3389-as port elérését</span><span class="sxs-lookup"><span data-stu-id="7f89c-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="7f89c-112">2. példa: hálózati biztonsági szabály létrehozása, amely lehetővé teszi a HTTP-t</span><span class="sxs-lookup"><span data-stu-id="7f89c-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="7f89c-113">Ez a parancs létrehoz egy biztonsági szabályt, amely lehetővé teszi az internetről a 80-as port elérését</span><span class="sxs-lookup"><span data-stu-id="7f89c-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="7f89c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f89c-114">PARAMETERS</span></span>

### <span data-ttu-id="7f89c-115">-Access</span><span class="sxs-lookup"><span data-stu-id="7f89c-115">-Access</span></span>
<span data-ttu-id="7f89c-116">Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.</span><span class="sxs-lookup"><span data-stu-id="7f89c-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="7f89c-117">A paraméter elfogadható értékei a következők: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="7f89c-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="7f89c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f89c-118">-DefaultProfile</span></span>
<span data-ttu-id="7f89c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f89c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f89c-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7f89c-120">-Description</span></span>
<span data-ttu-id="7f89c-121">A létrehozandó hálózati biztonsági szabály konfigurációjának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="7f89c-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7f89c-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="7f89c-123">A célcím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="7f89c-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f89c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f89c-125">Osztály nélküli tartományok közötti útválasztási (CIDR) cím</span><span class="sxs-lookup"><span data-stu-id="7f89c-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="7f89c-126">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="7f89c-126">A destination IP address range</span></span> 
- <span data-ttu-id="7f89c-127">A helyettesítő karakter (\*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.</span><span class="sxs-lookup"><span data-stu-id="7f89c-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="7f89c-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f89c-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="7f89c-129">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="7f89c-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7f89c-130">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="7f89c-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7f89c-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7f89c-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="7f89c-132">Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére.</span><span class="sxs-lookup"><span data-stu-id="7f89c-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7f89c-133">Az "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="7f89c-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7f89c-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="7f89c-134">-DestinationPortRange</span></span>
<span data-ttu-id="7f89c-135">A cél portját vagy a kívánt cellatartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="7f89c-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f89c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f89c-137">Egész szám</span><span class="sxs-lookup"><span data-stu-id="7f89c-137">An integer</span></span>
- <span data-ttu-id="7f89c-138">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="7f89c-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7f89c-139">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="7f89c-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="7f89c-140">-Irány</span><span class="sxs-lookup"><span data-stu-id="7f89c-140">-Direction</span></span>
<span data-ttu-id="7f89c-141">Azt adja meg, hogy a rendszer kiértékeli-e a szabályt a bejövő vagy kimenő forgalomban.</span><span class="sxs-lookup"><span data-stu-id="7f89c-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="7f89c-142">A paraméter elfogadható értékei a következők: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="7f89c-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="7f89c-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f89c-143">-Name</span></span>
<span data-ttu-id="7f89c-144">A parancsmag által létrehozott hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7f89c-145">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="7f89c-145">-Priority</span></span>
<span data-ttu-id="7f89c-146">A szabály konfigurációjának prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="7f89c-147">A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="7f89c-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="7f89c-148">A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.</span><span class="sxs-lookup"><span data-stu-id="7f89c-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="7f89c-149">Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="7f89c-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="7f89c-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7f89c-150">-Protocol</span></span>
<span data-ttu-id="7f89c-151">Azt a hálózati protokollt adja meg, amelyre az új szabály-konfiguráció vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="7f89c-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="7f89c-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f89c-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f89c-153">TCP</span><span class="sxs-lookup"><span data-stu-id="7f89c-153">Tcp</span></span>
- <span data-ttu-id="7f89c-154">UDP</span><span class="sxs-lookup"><span data-stu-id="7f89c-154">Udp</span></span>
- <span data-ttu-id="7f89c-155">a helyettesítő karakter (\*) a két érték egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="7f89c-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="7f89c-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7f89c-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="7f89c-157">A forráscím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="7f89c-158">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f89c-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f89c-159">CIDR</span><span class="sxs-lookup"><span data-stu-id="7f89c-159">A CIDR</span></span>
- <span data-ttu-id="7f89c-160">A forrás IP-köre</span><span class="sxs-lookup"><span data-stu-id="7f89c-160">A source IP range</span></span>
- <span data-ttu-id="7f89c-161">Egy helyettesítő karakter (\*) az IP-cím megegyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="7f89c-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="7f89c-162">A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f89c-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="7f89c-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f89c-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="7f89c-164">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="7f89c-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="7f89c-165">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="7f89c-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7f89c-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7f89c-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="7f89c-167">Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="7f89c-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="7f89c-168">Az "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="7f89c-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7f89c-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="7f89c-169">-SourcePortRange</span></span>
<span data-ttu-id="7f89c-170">A forrás portját vagy a tartománnyal adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f89c-170">Specifies the source port or range.</span></span>
<span data-ttu-id="7f89c-171">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f89c-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f89c-172">Egész szám</span><span class="sxs-lookup"><span data-stu-id="7f89c-172">An integer</span></span>
- <span data-ttu-id="7f89c-173">0 és 65535 közötti egész számok</span><span class="sxs-lookup"><span data-stu-id="7f89c-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7f89c-174">Bármely portnak megfelelő helyettesítő karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="7f89c-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="7f89c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f89c-175">CommonParameters</span></span>
<span data-ttu-id="7f89c-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f89c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f89c-177">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f89c-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f89c-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f89c-178">INPUTS</span></span>

### <span data-ttu-id="7f89c-179">Nincs</span><span class="sxs-lookup"><span data-stu-id="7f89c-179">None</span></span>

## <span data-ttu-id="7f89c-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f89c-180">OUTPUTS</span></span>

### <span data-ttu-id="7f89c-181">Microsoft. Azure. commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7f89c-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="7f89c-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f89c-182">NOTES</span></span>

## <span data-ttu-id="7f89c-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f89c-183">RELATED LINKS</span></span>

[<span data-ttu-id="7f89c-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f89c-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f89c-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f89c-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f89c-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f89c-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f89c-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f89c-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


