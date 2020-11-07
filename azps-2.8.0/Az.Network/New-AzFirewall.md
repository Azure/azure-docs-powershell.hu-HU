---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837215"
---
# <span data-ttu-id="7bb75-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7bb75-101">New-AzFirewall</span></span>

## <span data-ttu-id="7bb75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bb75-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb75-103">Új tűzfal létrehozása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="7bb75-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="7bb75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bb75-104">SYNTAX</span></span>

### <span data-ttu-id="7bb75-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7bb75-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb75-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="7bb75-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb75-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="7bb75-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bb75-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bb75-108">DESCRIPTION</span></span>
<span data-ttu-id="7bb75-109">A **New-AzFirewall** parancsmag Azure-tűzfalat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7bb75-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="7bb75-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7bb75-110">EXAMPLES</span></span>

### <span data-ttu-id="7bb75-111">1: virtuális hálózathoz kapcsolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="7bb75-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="7bb75-112">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="7bb75-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="7bb75-113">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).</span><span class="sxs-lookup"><span data-stu-id="7bb75-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="7bb75-114">Az Intel veszélyforrás az alapértelmezett módban is fut – riasztás – ami azt jelenti, hogy a kártékony forgalom naplózva lesz, de nem tagadható meg.</span><span class="sxs-lookup"><span data-stu-id="7bb75-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="7bb75-115">2: tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat</span><span class="sxs-lookup"><span data-stu-id="7bb75-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="7bb75-116">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi az összes HTTPS-forgalmat a 443-es porton keresztül.</span><span class="sxs-lookup"><span data-stu-id="7bb75-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="7bb75-117">Az Intel veszélyforrás az alapértelmezett módban fog futni – riasztás – ami azt jelenti, hogy a rendszer a kártékony forgalmat naplózza, de nem tagadja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb75-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="7bb75-118">3: DNAT-átirányítja a forgalmat a 10.1.2.3:80 – 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="7bb75-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="7bb75-119">Ez a példa létrehozta azt a tűzfalat, amely lefordította az 10.1.2.3-ra (80 – 10.2.3.4) irányuló összes csomag cél IP-portját: az 8080 veszélyforrás az Intel ki van kapcsolva ebben a példában.</span><span class="sxs-lookup"><span data-stu-id="7bb75-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="7bb75-120">4: szabály nélküli tűzfal létrehozása és az Intel veszélyforrása riasztás módban</span><span class="sxs-lookup"><span data-stu-id="7bb75-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="7bb75-121">Ez a példa létrehoz egy tűzfalat, amely blokkolja az összes forgalmat (az alapértelmezett viselkedést), és az Intel veszélyforrást jelenít meg riasztás módban.</span><span class="sxs-lookup"><span data-stu-id="7bb75-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="7bb75-122">Ez azt jelenti, hogy a rendszer riasztási naplókat bocsát ki a többi szabály alkalmazása előtt (ebben az esetben csak az alapértelmezett szabály: az összes elutasítása).</span><span class="sxs-lookup"><span data-stu-id="7bb75-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="7bb75-123">5: hozzon létre egy tűzfalat, amely lehetővé teszi az összes HTTP-forgalmat a 8080-on, de blokkolja az Intel által azonosított kártékony tartományokat.</span><span class="sxs-lookup"><span data-stu-id="7bb75-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="7bb75-124">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi a 8080-on lévő összes HTTP-forgalom beállítását, kivéve, ha az Intel veszélyezteti az adatokat.</span><span class="sxs-lookup"><span data-stu-id="7bb75-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="7bb75-125">Ha a Megtagadás üzemmódban fut, az értesítéstől eltérően az Intel által kártékonynak tekintett forgalom nem csak a naplózás, hanem a blokkolás is.</span><span class="sxs-lookup"><span data-stu-id="7bb75-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="7bb75-126">6: szabály nélküli tűzfal létrehozása és elérhetőségi zónák</span><span class="sxs-lookup"><span data-stu-id="7bb75-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="7bb75-127">Ez a példa létrehoz egy tűzfalat az összes elérhető elérhetőségi zónával.</span><span class="sxs-lookup"><span data-stu-id="7bb75-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="7bb75-128">7: tűzfal létrehozása két vagy több nyilvános IP-címről</span><span class="sxs-lookup"><span data-stu-id="7bb75-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="7bb75-129">Ez a példa létrehoz egy "vnet" virtuális hálózathoz kapcsolt tűzfalat két nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="7bb75-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="7bb75-130">8: tűzfal létrehozása, amely lehetővé teszi az MSSQL-forgalom adott SQL-adatbázishoz való elérését</span><span class="sxs-lookup"><span data-stu-id="7bb75-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="7bb75-131">Ebben a példában egy olyan tűzfal jön létre, amely lehetővé teszi az MSSQL-forgalomnak az 1433 standard porton való SQL-adatbázis sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="7bb75-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="7bb75-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bb75-132">PARAMETERS</span></span>

### <span data-ttu-id="7bb75-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7bb75-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="7bb75-134">Az új tűzfalhoz tartozó alkalmazási szabályok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb75-134">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bb75-135">-AsJob</span></span>
<span data-ttu-id="7bb75-136">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7bb75-136">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb75-137">-DefaultProfile</span></span>
<span data-ttu-id="7bb75-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bb75-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb75-139">-Force</span><span class="sxs-lookup"><span data-stu-id="7bb75-139">-Force</span></span>
<span data-ttu-id="7bb75-140">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7bb75-140">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-141">-Hely</span><span class="sxs-lookup"><span data-stu-id="7bb75-141">-Location</span></span>
<span data-ttu-id="7bb75-142">A tűzfal régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb75-142">Specifies the region for the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7bb75-143">-Name</span></span>
<span data-ttu-id="7bb75-144">Annak az Azure-tűzfalnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7bb75-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7bb75-145">-NatRuleCollection</span></span>
<span data-ttu-id="7bb75-146">A AzureFirewallNatRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="7bb75-146">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7bb75-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="7bb75-148">A AzureFirewallNetworkRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="7bb75-148">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7bb75-149">-PublicIpAddress</span></span>
<span data-ttu-id="7bb75-150">Egy vagy több nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="7bb75-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="7bb75-151">A nyilvános IP-címnek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="7bb75-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="7bb75-152">-PublicIpName</span></span>
<span data-ttu-id="7bb75-153">Nyilvános IP-név.</span><span class="sxs-lookup"><span data-stu-id="7bb75-153">Public Ip Name.</span></span> <span data-ttu-id="7bb75-154">A nyilvános IP-nek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="7bb75-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb75-155">-ResourceGroupName</span></span>
<span data-ttu-id="7bb75-156">Annak a csoportnak a neve, amely a tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7bb75-156">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-157">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="7bb75-157">-Zone</span></span>
<span data-ttu-id="7bb75-158">Az elérhetőségi zónák listája, amely azt jelzi, hogy a tűzfalnak hol kell származnia.</span><span class="sxs-lookup"><span data-stu-id="7bb75-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="7bb75-159">-Címke</span><span class="sxs-lookup"><span data-stu-id="7bb75-159">-Tag</span></span>
<span data-ttu-id="7bb75-160">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="7bb75-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7bb75-161">Példa:</span><span class="sxs-lookup"><span data-stu-id="7bb75-161">For example:</span></span>

<span data-ttu-id="7bb75-162">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="7bb75-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="7bb75-163">-ThreatIntelMode</span></span>
<span data-ttu-id="7bb75-164">A veszélyforrások felderítésének működési módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb75-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="7bb75-165">Az alapértelmezett üzemmód a riasztás, nem ki van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="7bb75-165">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bb75-166">-VirtualNetwork</span></span>
<span data-ttu-id="7bb75-167">Virtuális hálózat</span><span class="sxs-lookup"><span data-stu-id="7bb75-167">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7bb75-168">-VirtualNetworkName</span></span>
<span data-ttu-id="7bb75-169">Annak a virtuális hálózatnak a neve, amelybe a tűzfalat telepíteni fogják.</span><span class="sxs-lookup"><span data-stu-id="7bb75-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="7bb75-170">A virtuális hálózatnak és a tűzfalnak ugyanahhoz az erőforrás-csoporthoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="7bb75-170">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7bb75-171">-Confirm</span></span>
<span data-ttu-id="7bb75-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bb75-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb75-173">-WhatIf</span></span>
<span data-ttu-id="7bb75-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7bb75-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb75-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bb75-175">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb75-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb75-176">CommonParameters</span></span>
<span data-ttu-id="7bb75-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bb75-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb75-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb75-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb75-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bb75-179">INPUTS</span></span>

### <span data-ttu-id="7bb75-180">System. String</span><span class="sxs-lookup"><span data-stu-id="7bb75-180">System.String</span></span>

### <span data-ttu-id="7bb75-181">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bb75-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="7bb75-182">Microsoft. Azure. commands. Network. models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="7bb75-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="7bb75-183">Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="7bb75-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="7bb75-184">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="7bb75-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="7bb75-185">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="7bb75-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="7bb75-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7bb75-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7bb75-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bb75-187">OUTPUTS</span></span>

### <span data-ttu-id="7bb75-188">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7bb75-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7bb75-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bb75-189">NOTES</span></span>

## <span data-ttu-id="7bb75-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bb75-190">RELATED LINKS</span></span>

[<span data-ttu-id="7bb75-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7bb75-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7bb75-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7bb75-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="7bb75-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7bb75-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="7bb75-194">Új – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7bb75-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="7bb75-195">Új – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7bb75-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="7bb75-196">Új – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7bb75-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
