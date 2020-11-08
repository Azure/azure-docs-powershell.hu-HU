---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184861"
---
# <span data-ttu-id="253d1-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="253d1-101">New-AzFirewall</span></span>

## <span data-ttu-id="253d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="253d1-102">SYNOPSIS</span></span>
<span data-ttu-id="253d1-103">Új tűzfal létrehozása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="253d1-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="253d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="253d1-104">SYNTAX</span></span>

### <span data-ttu-id="253d1-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="253d1-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="253d1-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="253d1-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="253d1-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="253d1-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="253d1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="253d1-108">DESCRIPTION</span></span>
<span data-ttu-id="253d1-109">A **New-AzFirewall** parancsmag Azure-tűzfalat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="253d1-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="253d1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="253d1-110">EXAMPLES</span></span>

### <span data-ttu-id="253d1-111">Példa 1: virtuális hálózathoz kapcsolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="253d1-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="253d1-112">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="253d1-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="253d1-113">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).</span><span class="sxs-lookup"><span data-stu-id="253d1-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="253d1-114">Az Intel veszélyforrás az alapértelmezett módban is fut – riasztás – ami azt jelenti, hogy a kártékony forgalom naplózva lesz, de nem tagadható meg.</span><span class="sxs-lookup"><span data-stu-id="253d1-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="253d1-115">2. példa: tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat</span><span class="sxs-lookup"><span data-stu-id="253d1-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="253d1-116">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi az összes HTTPS-forgalmat a 443-es porton keresztül.</span><span class="sxs-lookup"><span data-stu-id="253d1-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="253d1-117">Az Intel veszélyforrás az alapértelmezett módban fog futni – riasztás – ami azt jelenti, hogy a rendszer a kártékony forgalmat naplózza, de nem tagadja meg.</span><span class="sxs-lookup"><span data-stu-id="253d1-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="253d1-118">3. példa: DNAT-átirányítja a 10.1.2.3:80 – 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="253d1-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="253d1-119">Ez a példa létrehozta azt a tűzfalat, amely lefordította az 10.1.2.3-ra (80 – 10.2.3.4) irányuló összes csomag cél IP-portját: az 8080 veszélyforrás az Intel ki van kapcsolva ebben a példában.</span><span class="sxs-lookup"><span data-stu-id="253d1-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="253d1-120">Példa 4: a szabályok nélküli tűzfal és az Intel fenyegetésekkel való létrehozása riasztási üzemmódban</span><span class="sxs-lookup"><span data-stu-id="253d1-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="253d1-121">Ez a példa létrehoz egy tűzfalat, amely blokkolja az összes forgalmat (az alapértelmezett viselkedést), és az Intel veszélyforrást jelenít meg riasztás módban.</span><span class="sxs-lookup"><span data-stu-id="253d1-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="253d1-122">Ez azt jelenti, hogy a rendszer riasztási naplókat bocsát ki a többi szabály alkalmazása előtt (ebben az esetben csak az alapértelmezett szabály: az összes elutasítása).</span><span class="sxs-lookup"><span data-stu-id="253d1-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="253d1-123">Példa 5: tűzfal létrehozása, amely lehetővé teszi az összes HTTP-forgalom engedélyezését a 8080-on, de blokkolja az Intel fenyegetések által azonosított kártékony tartományokat</span><span class="sxs-lookup"><span data-stu-id="253d1-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="253d1-124">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi a 8080-on lévő összes HTTP-forgalom beállítását, kivéve, ha az Intel veszélyezteti az adatokat.</span><span class="sxs-lookup"><span data-stu-id="253d1-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="253d1-125">Ha a Megtagadás üzemmódban fut, az értesítéstől eltérően az Intel által kártékonynak tekintett forgalom nem csak a naplózás, hanem a blokkolás is.</span><span class="sxs-lookup"><span data-stu-id="253d1-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="253d1-126">6. példa: szabály nélküli tűzfal létrehozása és elérhetőségi zónák</span><span class="sxs-lookup"><span data-stu-id="253d1-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="253d1-127">Ez a példa létrehoz egy tűzfalat az összes elérhető elérhetőségi zónával.</span><span class="sxs-lookup"><span data-stu-id="253d1-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="253d1-128">7. példa: tűzfal létrehozása két vagy több nyilvános IP-címről</span><span class="sxs-lookup"><span data-stu-id="253d1-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="253d1-129">Ez a példa létrehoz egy "vnet" virtuális hálózathoz kapcsolt tűzfalat két nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="253d1-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="253d1-130">8. példa: tűzfal létrehozása, amely lehetővé teszi az MSSQL-forgalom adott SQL-adatbázishoz való elérését</span><span class="sxs-lookup"><span data-stu-id="253d1-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="253d1-131">Ebben a példában egy olyan tűzfal jön létre, amely lehetővé teszi az MSSQL-forgalomnak az 1433 standard porton való SQL-adatbázis sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="253d1-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="253d1-132">Példa 9: virtuális hubhoz kapcsolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="253d1-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="253d1-133">Ez a példa létrehoz egy tűzfalat, amely a Virtual hub "vHub" hivatkozással van társítva.</span><span class="sxs-lookup"><span data-stu-id="253d1-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="253d1-134">Tűzfal-házirend $fp a tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="253d1-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="253d1-135">Ez a tűzfal engedélyezi/megtagadja a forgalmat a tűzfal házirend-$fpban említett szabályok alapján.</span><span class="sxs-lookup"><span data-stu-id="253d1-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="253d1-136">A virtuális hub és a tűzfalnak ugyanabban a régióban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="253d1-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="253d1-137">10 példa: tűzfal létrehozása veszélyforrást tartalmazó intelligencia whitelist beállítással</span><span class="sxs-lookup"><span data-stu-id="253d1-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="253d1-138">Ez a példa létrehoz egy tűzfalat, amely a "www.microsoft.com" és a "8.8.8.8" whitelist-ról a fenyegetések elleni intelligenciáról szól.</span><span class="sxs-lookup"><span data-stu-id="253d1-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="253d1-139">Példa 11: tűzfal létrehozása testreszabott privát tartománnyal beállítással</span><span class="sxs-lookup"><span data-stu-id="253d1-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="253d1-140">Ebben a példában egy olyan tűzfal jön létre, amely a "99.99.99.0/24" és a "66.66.0.0/16" privát IP-tartományokat kezeli, és nem SNAT a forgalmat a címekre</span><span class="sxs-lookup"><span data-stu-id="253d1-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="253d1-141">12 példa: tűzfal létrehozása felügyeleti alhálózattal és nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="253d1-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="253d1-142">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="253d1-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="253d1-143">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).</span><span class="sxs-lookup"><span data-stu-id="253d1-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="253d1-144">Az Intel veszélyforrás az alapértelmezett módban is fut – riasztás – ami azt jelenti, hogy a kártékony forgalom naplózva lesz, de nem tagadható meg.</span><span class="sxs-lookup"><span data-stu-id="253d1-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="253d1-145">A "kényszerített bújtatás" forgatókönyvek támogatása érdekében ez a tűzfal a "AzureFirewallManagementSubnet" alhálózatot fogja használni, és a felügyeleti központot a felügyeleti forgalomhoz tartozó nyilvános IP-címen</span><span class="sxs-lookup"><span data-stu-id="253d1-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="253d1-146">Példa: tűzfal létrehozása virtuális hálózathoz kapcsolódó tűzfal-házirenddel</span><span class="sxs-lookup"><span data-stu-id="253d1-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="253d1-147">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="253d1-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="253d1-148">A tűzfalra alkalmazott szabályok és veszélyforrások intelligencia a tűzfal házirendjében fog megjelenni.</span><span class="sxs-lookup"><span data-stu-id="253d1-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="253d1-149">14 példa: tűzfal létrehozása DNS-proxyval és DNS-kiszolgálókkal</span><span class="sxs-lookup"><span data-stu-id="253d1-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="253d1-150">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="253d1-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="253d1-151">Engedélyezve van a DNS-proxy a tűzfalon, és 2 DNS-kiszolgáló van megadva.</span><span class="sxs-lookup"><span data-stu-id="253d1-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="253d1-152">Szükség van-e arra is, hogy a hálózati szabályokhoz a DNS-proxy legyen beállítva, így ha vannak olyan hálózati szabályok, amelyek FQDN-jei, akkor a rendszer a DNS-proxyt fogja használni.</span><span class="sxs-lookup"><span data-stu-id="253d1-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="253d1-153">15 példa: hozzon létre egy több IP-t tartalmazó tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="253d1-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="253d1-154">A tűzfal társítható a virtuális hubhoz</span><span class="sxs-lookup"><span data-stu-id="253d1-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="253d1-155">Ez a példa létrehoz egy tűzfalat a virtuális hub "hub"-hoz társított tűzfalban.</span><span class="sxs-lookup"><span data-stu-id="253d1-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="253d1-156">A tűzfal két nyilvános IP-t fog kiosztani, amelyek implicit módon jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="253d1-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="253d1-157">16: hozzon létre egy tűzfalat, és engedélyezze az aktív FTP-t.</span><span class="sxs-lookup"><span data-stu-id="253d1-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="253d1-158">Ez a példa tűzfalat hoz létre az aktív FTP-jelölő engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="253d1-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="253d1-159">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="253d1-159">PARAMETERS</span></span>

### <span data-ttu-id="253d1-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="253d1-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="253d1-161">Az új tűzfalhoz tartozó alkalmazási szabályok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="253d1-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="253d1-162">-AsJob</span></span>
<span data-ttu-id="253d1-163">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="253d1-163">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253d1-164">-DefaultProfile</span></span>
<span data-ttu-id="253d1-165">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="253d1-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="253d1-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="253d1-167">A hálózati szabályokban a DNS-proxy funkció a teljes tartománynevek esetén szükséges.</span><span class="sxs-lookup"><span data-stu-id="253d1-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="253d1-168">-DnsServer</span></span>
<span data-ttu-id="253d1-169">A DNS-feloldáshoz használandó DNS-kiszolgálók listája</span><span class="sxs-lookup"><span data-stu-id="253d1-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="253d1-170">-EnableDnsProxy</span></span>
<span data-ttu-id="253d1-171">Engedélyezze a DNS-proxyt.</span><span class="sxs-lookup"><span data-stu-id="253d1-171">Enable DNS Proxy.</span></span> <span data-ttu-id="253d1-172">Alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="253d1-172">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="253d1-173">-AllowActiveFTP</span></span>
<span data-ttu-id="253d1-174">Engedélyezi az aktív FTP-t a tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="253d1-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="253d1-175">Alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="253d1-175">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="253d1-176">-FirewallPolicyId</span></span>
<span data-ttu-id="253d1-177">A tűzfalhoz társított tűzfal-házirend</span><span class="sxs-lookup"><span data-stu-id="253d1-177">The firewall policy attached to the firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-178">-Force</span><span class="sxs-lookup"><span data-stu-id="253d1-178">-Force</span></span>
<span data-ttu-id="253d1-179">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="253d1-179">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="253d1-180">-HubIPAddresses</span></span>
<span data-ttu-id="253d1-181">A virtuális hubhoz kapcsolt tűzfal IP-címei</span><span class="sxs-lookup"><span data-stu-id="253d1-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-182">-Hely</span><span class="sxs-lookup"><span data-stu-id="253d1-182">-Location</span></span>
<span data-ttu-id="253d1-183">A tűzfal régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="253d1-183">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="253d1-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="253d1-185">Egy vagy több nyilvános IP-cím, amelyet a kezelési forgalomhoz szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="253d1-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="253d1-186">A nyilvános IP-címnek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="253d1-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-187">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="253d1-187">-Name</span></span>
<span data-ttu-id="253d1-188">Annak az Azure-tűzfalnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="253d1-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="253d1-189">-NatRuleCollection</span></span>
<span data-ttu-id="253d1-190">A AzureFirewallNatRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="253d1-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="253d1-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="253d1-192">A AzureFirewallNetworkRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="253d1-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="253d1-193">-PrivateRange</span></span>
<span data-ttu-id="253d1-194">Azok a privát IP-tartományok, amelyeken a forgalom nem lesz SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="253d1-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="253d1-195">-PublicIpAddress</span></span>
<span data-ttu-id="253d1-196">Egy vagy több nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="253d1-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="253d1-197">A nyilvános IP-címnek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="253d1-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="253d1-198">-PublicIpName</span></span>
<span data-ttu-id="253d1-199">Nyilvános IP-név.</span><span class="sxs-lookup"><span data-stu-id="253d1-199">Public Ip Name.</span></span> <span data-ttu-id="253d1-200">A nyilvános IP-nek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="253d1-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="253d1-201">-ResourceGroupName</span></span>
<span data-ttu-id="253d1-202">Annak a csoportnak a neve, amely a tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="253d1-202">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-203">-SKU</span><span class="sxs-lookup"><span data-stu-id="253d1-203">-Sku</span></span>
<span data-ttu-id="253d1-204">A tűzfal SKU-típusa</span><span class="sxs-lookup"><span data-stu-id="253d1-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-205">-Címke</span><span class="sxs-lookup"><span data-stu-id="253d1-205">-Tag</span></span>
<span data-ttu-id="253d1-206">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="253d1-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="253d1-207">Példa:</span><span class="sxs-lookup"><span data-stu-id="253d1-207">For example:</span></span>

<span data-ttu-id="253d1-208">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="253d1-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="253d1-209">-ThreatIntelMode</span></span>
<span data-ttu-id="253d1-210">A veszélyforrások felderítésének működési módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="253d1-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="253d1-211">Az alapértelmezett üzemmód a riasztás, nem ki van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="253d1-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="253d1-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="253d1-213">A fenyegetések elleni intelligencia whitelist (whitelist)</span><span class="sxs-lookup"><span data-stu-id="253d1-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="253d1-214">-VirtualHubId</span></span>
<span data-ttu-id="253d1-215">A tűzfal által társított virtuális hub</span><span class="sxs-lookup"><span data-stu-id="253d1-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="253d1-216">-VirtualNetwork</span></span>
<span data-ttu-id="253d1-217">Virtuális hálózat</span><span class="sxs-lookup"><span data-stu-id="253d1-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="253d1-218">-VirtualNetworkName</span></span>
<span data-ttu-id="253d1-219">Annak a virtuális hálózatnak a neve, amelybe a tűzfalat telepíteni fogják.</span><span class="sxs-lookup"><span data-stu-id="253d1-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="253d1-220">A virtuális hálózatnak és a tűzfalnak ugyanahhoz az erőforrás-csoporthoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="253d1-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-221">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="253d1-221">-Zone</span></span>
<span data-ttu-id="253d1-222">Az elérhetőségi zónák listája, amely azt jelzi, hogy a tűzfalnak hol kell származnia.</span><span class="sxs-lookup"><span data-stu-id="253d1-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-223">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="253d1-223">-Confirm</span></span>
<span data-ttu-id="253d1-224">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="253d1-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="253d1-225">-WhatIf</span></span>
<span data-ttu-id="253d1-226">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="253d1-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="253d1-227">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="253d1-227">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d1-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253d1-228">CommonParameters</span></span>
<span data-ttu-id="253d1-229">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="253d1-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253d1-230">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="253d1-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253d1-231">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="253d1-231">INPUTS</span></span>

### <span data-ttu-id="253d1-232">System. String</span><span class="sxs-lookup"><span data-stu-id="253d1-232">System.String</span></span>

### <span data-ttu-id="253d1-233">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="253d1-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="253d1-234">Microsoft. Azure. commands. Network. models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="253d1-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="253d1-235">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="253d1-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="253d1-236">Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="253d1-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="253d1-237">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="253d1-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="253d1-238">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="253d1-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="253d1-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="253d1-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="253d1-240">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="253d1-240">OUTPUTS</span></span>

### <span data-ttu-id="253d1-241">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="253d1-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="253d1-242">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="253d1-242">NOTES</span></span>

## <span data-ttu-id="253d1-243">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="253d1-243">RELATED LINKS</span></span>

[<span data-ttu-id="253d1-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="253d1-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="253d1-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="253d1-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="253d1-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="253d1-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="253d1-247">Új – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="253d1-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="253d1-248">Új – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="253d1-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="253d1-249">Új – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="253d1-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
