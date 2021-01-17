---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340722"
---
# <span data-ttu-id="8e425-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e425-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8e425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e425-102">SYNOPSIS</span></span>
<span data-ttu-id="8e425-103">Hálózati biztonsági szabály konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8e425-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="8e425-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e425-104">SYNTAX</span></span>

### <span data-ttu-id="8e425-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e425-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e425-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e425-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e425-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e425-107">DESCRIPTION</span></span>
<span data-ttu-id="8e425-108">A **New-AzNetworkSecurityRuleConfig** parancsmag létrehoz egy Azure-hálózatbiztonsági szabálykonfigurációt egy hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="8e425-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8e425-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e425-109">EXAMPLES</span></span>

### <span data-ttu-id="8e425-110">1. példa: Az RDP-t engedélyező hálózati biztonsági szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="8e425-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="8e425-111">Ez a parancs egy olyan biztonsági szabályt hoz létre, amely engedélyezi az internetről a 3389-es port elérését</span><span class="sxs-lookup"><span data-stu-id="8e425-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="8e425-112">2. példa: HTTP-t lehetővé tő hálózati biztonsági szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="8e425-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="8e425-113">Ez a parancs egy olyan biztonsági szabályt hoz létre, amely engedélyezi az internetről a 80-as portot</span><span class="sxs-lookup"><span data-stu-id="8e425-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="8e425-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e425-114">PARAMETERS</span></span>

### <span data-ttu-id="8e425-115">-Access</span><span class="sxs-lookup"><span data-stu-id="8e425-115">-Access</span></span>
<span data-ttu-id="8e425-116">Azt adja meg, hogy engedélyezett vagy megtagadható-e a hálózati forgalom.</span><span class="sxs-lookup"><span data-stu-id="8e425-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="8e425-117">A paraméter elfogadható értékei: Allow és Deny.</span><span class="sxs-lookup"><span data-stu-id="8e425-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="8e425-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e425-118">-DefaultProfile</span></span>
<span data-ttu-id="8e425-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e425-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e425-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8e425-120">-Description</span></span>
<span data-ttu-id="8e425-121">Megadja a létrehozni szükséges hálózati biztonsági szabály konfigurációjának leírását.</span><span class="sxs-lookup"><span data-stu-id="8e425-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="8e425-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8e425-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="8e425-123">Megadja a célcím előtagját.</span><span class="sxs-lookup"><span data-stu-id="8e425-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="8e425-124">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8e425-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e425-125">A Classless Interdomain Routing (CIDR) address</span><span class="sxs-lookup"><span data-stu-id="8e425-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="8e425-126">Cél IP-címtartomány</span><span class="sxs-lookup"><span data-stu-id="8e425-126">A destination IP address range</span></span> 
- <span data-ttu-id="8e425-127">Helyettesítő karakter (\*) bármely IP-címhez. Használhat például VirtualNetwork, AzureLoadBalancer és Internet címkéket.</span><span class="sxs-lookup"><span data-stu-id="8e425-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="8e425-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e425-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="8e425-129">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="8e425-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8e425-130">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="8e425-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8e425-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8e425-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="8e425-132">A szabály célhelyének beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="8e425-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8e425-133">A "DestinationAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="8e425-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8e425-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="8e425-134">-DestinationPortRange</span></span>
<span data-ttu-id="8e425-135">Célportot vagy tartományt ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e425-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="8e425-136">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8e425-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e425-137">Egész szám</span><span class="sxs-lookup"><span data-stu-id="8e425-137">An integer</span></span>
- <span data-ttu-id="8e425-138">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="8e425-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8e425-139">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="8e425-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="8e425-140">-Irány</span><span class="sxs-lookup"><span data-stu-id="8e425-140">-Direction</span></span>
<span data-ttu-id="8e425-141">Meghatározza, hogy egy szabály kiértékelve legyen-e a bejövő vagy kimenő forgalom esetén.</span><span class="sxs-lookup"><span data-stu-id="8e425-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="8e425-142">A paraméter elfogadható értékei a következőek: Bejövő és Kimenő.</span><span class="sxs-lookup"><span data-stu-id="8e425-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="8e425-143">-Name</span><span class="sxs-lookup"><span data-stu-id="8e425-143">-Name</span></span>
<span data-ttu-id="8e425-144">A parancsmag által létrehozott hálózati biztonsági szabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e425-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8e425-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="8e425-145">-Priority</span></span>
<span data-ttu-id="8e425-146">Meghatározza a szabálykonfiguráció prioritását.</span><span class="sxs-lookup"><span data-stu-id="8e425-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="8e425-147">A paraméter elfogadható értékei: Egy 100 és 4096 közötti egész szám.</span><span class="sxs-lookup"><span data-stu-id="8e425-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="8e425-148">A prioritásszámnak egyedinek kell lennie a gyűjtemény minden egyes szabályában.</span><span class="sxs-lookup"><span data-stu-id="8e425-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="8e425-149">Minél kisebb a prioritási szám, annál nagyobb a szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="8e425-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="8e425-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8e425-150">-Protocol</span></span>
<span data-ttu-id="8e425-151">Azt a hálózati protokollt adja meg, amelyre az új szabálykonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="8e425-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="8e425-152">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8e425-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e425-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="8e425-153">Tcp</span></span>
- <span data-ttu-id="8e425-154">Udp</span><span class="sxs-lookup"><span data-stu-id="8e425-154">Udp</span></span>
- <span data-ttu-id="8e425-155">helyettesítő karakter (\*) mindkét esetben</span><span class="sxs-lookup"><span data-stu-id="8e425-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="8e425-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8e425-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="8e425-157">Megadja a forráscím előtagját.</span><span class="sxs-lookup"><span data-stu-id="8e425-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="8e425-158">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8e425-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e425-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="8e425-159">A CIDR</span></span>
- <span data-ttu-id="8e425-160">Forrás IP-tartomány</span><span class="sxs-lookup"><span data-stu-id="8e425-160">A source IP range</span></span>
- <span data-ttu-id="8e425-161">Egy tetszőleges IP-címnek megfelelő helyettesítő karakter (\*).</span><span class="sxs-lookup"><span data-stu-id="8e425-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="8e425-162">Használhat olyan címkéket is, mint a VirtualNetwork, az AzureLoadBalancer és az internet.</span><span class="sxs-lookup"><span data-stu-id="8e425-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="8e425-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e425-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="8e425-164">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="8e425-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="8e425-165">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="8e425-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8e425-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8e425-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="8e425-167">A szabály forrásaként beállított alkalmazásbiztonsági csoport.</span><span class="sxs-lookup"><span data-stu-id="8e425-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="8e425-168">A "SourceAddressPrefix" paraméterrel nem használható.</span><span class="sxs-lookup"><span data-stu-id="8e425-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8e425-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="8e425-169">-SourcePortRange</span></span>
<span data-ttu-id="8e425-170">A forrásportot vagy -tartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e425-170">Specifies the source port or range.</span></span>
<span data-ttu-id="8e425-171">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8e425-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e425-172">Egész szám</span><span class="sxs-lookup"><span data-stu-id="8e425-172">An integer</span></span>
- <span data-ttu-id="8e425-173">A 0 és 65535 közötti egész számtartomány</span><span class="sxs-lookup"><span data-stu-id="8e425-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8e425-174">Helyettesítő karakter (\*) egy tetszőleges porthoz</span><span class="sxs-lookup"><span data-stu-id="8e425-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="8e425-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e425-175">CommonParameters</span></span>
<span data-ttu-id="8e425-176">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e425-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e425-177">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e425-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e425-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e425-178">INPUTS</span></span>

### <span data-ttu-id="8e425-179">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e425-179">None</span></span>

## <span data-ttu-id="8e425-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e425-180">OUTPUTS</span></span>

### <span data-ttu-id="8e425-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="8e425-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="8e425-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e425-182">NOTES</span></span>

## <span data-ttu-id="8e425-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e425-183">RELATED LINKS</span></span>

[<span data-ttu-id="8e425-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e425-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8e425-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e425-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8e425-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e425-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8e425-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e425-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


