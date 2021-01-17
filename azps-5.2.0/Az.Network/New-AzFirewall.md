---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335202"
---
# <span data-ttu-id="73278-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73278-101">New-AzFirewall</span></span>

## <span data-ttu-id="73278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73278-102">SYNOPSIS</span></span>
<span data-ttu-id="73278-103">Létrehoz egy új tűzfalat egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="73278-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="73278-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73278-104">SYNTAX</span></span>

### <span data-ttu-id="73278-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73278-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73278-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="73278-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73278-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="73278-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73278-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73278-108">DESCRIPTION</span></span>
<span data-ttu-id="73278-109">A **New-AzFirewall** parancsmag létrehoz egy Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="73278-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="73278-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73278-110">EXAMPLES</span></span>

### <span data-ttu-id="73278-111">1. példa: Virtuális hálózathoz csatolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="73278-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="73278-112">Ebben a példában létrehoz egy tűzfalat, amely a virtuális hálózat "vnet" hálózatához van csatolva ugyanabban az erőforráscsoportban, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="73278-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="73278-113">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (ez az alapértelmezett működés).</span><span class="sxs-lookup"><span data-stu-id="73278-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="73278-114">A Threat Intel is az alapértelmezett módban fog futni – riasztás – ami azt jelenti, hogy a kártékony forgalmat naplózza a rendszer, de nem utasítja el.</span><span class="sxs-lookup"><span data-stu-id="73278-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="73278-115">2. példa: Tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat</span><span class="sxs-lookup"><span data-stu-id="73278-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="73278-116">Ebben a példában egy tűzfalat hozunk létre, amely lehetővé teszi az összes HTTPS-forgalmat a 443-as porton.</span><span class="sxs-lookup"><span data-stu-id="73278-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="73278-117">A Threat Intel az alapértelmezett módban (Riasztás) fut, ami azt jelenti, hogy a kártékony forgalmat naplózza a rendszer, de nem utasítja el.</span><span class="sxs-lookup"><span data-stu-id="73278-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="73278-118">3. példa: A 10.1.2.3:80-as és 10.2.3.4:8080-as kódú forgalom átirányítása</span><span class="sxs-lookup"><span data-stu-id="73278-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="73278-119">Ebben a példában egy tűzfal jött létre, amely lefordította a cél IP-címét és az összes csomag portját, amely a 10.1.2.3:80-as és a 10.2.3.4.4:8080 Threat Intel-re lett lefordítva ebben a példában.</span><span class="sxs-lookup"><span data-stu-id="73278-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="73278-120">4. példa: Tűzfal létrehozása szabályok nélkül és a Threat Intel riasztási módban</span><span class="sxs-lookup"><span data-stu-id="73278-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="73278-121">Ebben a példában egy tűzfalat hoz létre, amely letiltja az összes forgalmat (alapértelmezett működés), és a Threat Intel riasztási módban fut.</span><span class="sxs-lookup"><span data-stu-id="73278-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="73278-122">Ez azt jelenti, hogy a többi szabály alkalmazása előtt figyelmeztetést küld a naplókról a kártékony adatforgalomhoz (ebben az esetben csak az alapértelmezett szabály – Az összes elutasítása)</span><span class="sxs-lookup"><span data-stu-id="73278-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="73278-123">5. példa: Tűzfal létrehozása, amely lehetővé teszi az összes HTTP-adatforgalmat a 8080-as porton, de letiltja a Threat Intel által azonosított kártékony tartományokat</span><span class="sxs-lookup"><span data-stu-id="73278-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="73278-124">Ebben a példában egy tűzfalat hoz létre, amely lehetővé teszi a 8080-as port összes HTTP-adatforgalmát, kivéve ha a Threat Intel kártékonynak tekintette.</span><span class="sxs-lookup"><span data-stu-id="73278-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="73278-125">Az Elutasítás módban a Riasztástól eltérően a Threat Intel által kártékonynak tekintett adatforgalom nem csak naplózva, hanem blokkolva is van.</span><span class="sxs-lookup"><span data-stu-id="73278-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="73278-126">6. példa: Tűzfal létrehozása szabályok és elérhetőségi zónák nélkül</span><span class="sxs-lookup"><span data-stu-id="73278-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="73278-127">Ebben a példában egy tűzfalat hoz létre az összes rendelkezésre álló elérhetőségi zónával.</span><span class="sxs-lookup"><span data-stu-id="73278-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="73278-128">7. példa: Tűzfal létrehozása két vagy több nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="73278-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="73278-129">Ebben a példában létrehoz egy tűzfalat, amely két nyilvános IP-címmel rendelkezik a virtuális "vnet" hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="73278-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="73278-130">8. példa: Tűzfal létrehozása, amely lehetővé teszi az MSSQL-adatforgalom adott SQL-adatbázisba való forgalmát</span><span class="sxs-lookup"><span data-stu-id="73278-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="73278-131">Ebben a példában egy tűzfalat hoz létre, amely lehetővé teszi az MSSQL-adatforgalmat a szabványos 1433-as porton az SQL-sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="73278-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="73278-132">9. példa: Virtuális központhoz csatolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="73278-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="73278-133">Ebben a példában létrehoz egy tűzfalat, amely a virtuális "vHub" központhoz van csatolva.</span><span class="sxs-lookup"><span data-stu-id="73278-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="73278-134">A tűzfalhoz $fp egy tűzfal-házirendet.</span><span class="sxs-lookup"><span data-stu-id="73278-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="73278-135">Ez a tűzfal engedélyezi/letiltja a forgalmat a tűzfal-házirendben említett szabályok $fp.</span><span class="sxs-lookup"><span data-stu-id="73278-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="73278-136">A virtuális központnak és a tűzfalnak ugyanabban a régióban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="73278-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="73278-137">10. példa: Tűzfal létrehozása a veszélyforrás-felderítési whitelistával</span><span class="sxs-lookup"><span data-stu-id="73278-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="73278-138">Ebben a példában egy tűzfalat hoz létre, amely a "www.microsoft.com" és a "8.8.8.8" listát hozza létre a veszélyforrás-felderítésből</span><span class="sxs-lookup"><span data-stu-id="73278-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="73278-139">11. példa: Tűzfal létrehozása testre szabott privát tartománybeállítással</span><span class="sxs-lookup"><span data-stu-id="73278-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="73278-140">Ebben a példában egy olyan tűzfalat hoz létre, amely a "99.99.99.0/24" és a "66.66.0.0/16" ip-címtartományt magánjellegű IP-tartományként kezeli, és nem fogja e címek forgalmát elgépelni.</span><span class="sxs-lookup"><span data-stu-id="73278-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="73278-141">12. példa: Tűzfal létrehozása felügyeleti alhálózatmal és nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="73278-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="73278-142">Ebben a példában létrehoz egy tűzfalat, amely a virtuális hálózat "vnet" hálózatához van csatolva ugyanabban az erőforráscsoportban, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="73278-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="73278-143">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (ez az alapértelmezett működés).</span><span class="sxs-lookup"><span data-stu-id="73278-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="73278-144">A Threat Intel is az alapértelmezett módban fog futni – riasztás – ami azt jelenti, hogy a kártékony forgalmat naplózza a rendszer, de nem utasítja el.</span><span class="sxs-lookup"><span data-stu-id="73278-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="73278-145">A "kényszerített alagutasítás" eset támogatása érdekében ez a tűzfal az "AzureFirewallManagementSubnet" alhálózatot és a felügyeleti nyilvános IP-címet fogja használni a felügyeleti forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="73278-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="73278-146">13. példa: Tűzfal létrehozása virtuális hálózathoz csatolt tűzfal-házirend segítségével</span><span class="sxs-lookup"><span data-stu-id="73278-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="73278-147">Ebben a példában létrehoz egy tűzfalat, amely a virtuális hálózat "vnet" hálózatához van csatolva ugyanabban az erőforráscsoportban, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="73278-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="73278-148">A tűzfalra vonatkozó szabályok és veszélyforrás-felderítések a tűzfal házirendből fognak átesni</span><span class="sxs-lookup"><span data-stu-id="73278-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="73278-149">14. példa: Tűzfal létrehozása DNS-proxyval és DNS-kiszolgálókkal</span><span class="sxs-lookup"><span data-stu-id="73278-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="73278-150">Ebben a példában létrehoz egy tűzfalat, amely a virtuális hálózat "vnet" hálózatához van csatolva ugyanabban az erőforráscsoportban, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="73278-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="73278-151">A tűzfalhoz engedélyezve van a DNS-proxy, és 2 DNS-kiszolgáló is rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="73278-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="73278-152">Emellett a Hálózati DNS-proxy megkövetelése szabályok is be vannak állítva, így ha vannak teljes tartományneveket is szolgáltató hálózati szabályok, akkor a RENDSZER a DNS-proxyt is használni fogja.</span><span class="sxs-lookup"><span data-stu-id="73278-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="73278-153">15. példa: Tűzfal létrehozása több IP-t használva.</span><span class="sxs-lookup"><span data-stu-id="73278-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="73278-154">A tűzfal társítható a virtuális központhoz</span><span class="sxs-lookup"><span data-stu-id="73278-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="73278-155">Ebben a példában létrehoz egy tűzfalat, amely a virtuális központhoz kapcsolódik ugyanabban az erőforráscsoportban, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="73278-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="73278-156">A tűzfalhoz 2 nyilvános, implicit módon létrehozott IP-t rendelünk hozzá.</span><span class="sxs-lookup"><span data-stu-id="73278-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="73278-157">16: Tűzfal létrehozása az Aktív FTP engedélyezése parancsokkal.</span><span class="sxs-lookup"><span data-stu-id="73278-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="73278-158">Ebben a példában egy tűzfalat hoz létre, amely engedélyezi az aktív FTP-jelzőt.</span><span class="sxs-lookup"><span data-stu-id="73278-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="73278-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73278-159">PARAMETERS</span></span>

### <span data-ttu-id="73278-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="73278-160">-AllowActiveFTP</span></span>
<span data-ttu-id="73278-161">Engedélyezi az aktív FTP-t a tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="73278-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="73278-162">Alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="73278-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="73278-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73278-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="73278-164">Az új tűzfal alkalmazásszabály-gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73278-164">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="73278-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73278-165">-AsJob</span></span>
<span data-ttu-id="73278-166">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73278-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73278-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73278-167">-DefaultProfile</span></span>
<span data-ttu-id="73278-168">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73278-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73278-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="73278-169">-DnsServer</span></span>
<span data-ttu-id="73278-170">A DNS-megoldáshoz használt DNS-kiszolgálók listája,</span><span class="sxs-lookup"><span data-stu-id="73278-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="73278-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="73278-171">-EnableDnsProxy</span></span>
<span data-ttu-id="73278-172">Engedélyezze a DNS-proxyt.</span><span class="sxs-lookup"><span data-stu-id="73278-172">Enable DNS Proxy.</span></span> <span data-ttu-id="73278-173">Alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="73278-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="73278-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="73278-174">-FirewallPolicyId</span></span>
<span data-ttu-id="73278-175">A tűzfalhoz csatolt tűzfal-házirend</span><span class="sxs-lookup"><span data-stu-id="73278-175">The firewall policy attached to the firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73278-176">-Force</span><span class="sxs-lookup"><span data-stu-id="73278-176">-Force</span></span>
<span data-ttu-id="73278-177">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="73278-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73278-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="73278-178">-HubIPAddress</span></span>
<span data-ttu-id="73278-179">A virtuális központhoz csatolt tűzfal IP-címei</span><span class="sxs-lookup"><span data-stu-id="73278-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73278-180">-Location</span><span class="sxs-lookup"><span data-stu-id="73278-180">-Location</span></span>
<span data-ttu-id="73278-181">A tűzfal régióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="73278-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="73278-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="73278-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="73278-183">Egy vagy több nyilvános IP-cím, amelyek a forgalom kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="73278-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="73278-184">A nyilvános IP-címeknek szabványos termékváltozatot kell használniuk, és a tűzfallal azonos erőforráscsoporthoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="73278-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73278-185">-Name</span><span class="sxs-lookup"><span data-stu-id="73278-185">-Name</span></span>
<span data-ttu-id="73278-186">A parancsmag által létrehozott Azure Tűzfal neve.</span><span class="sxs-lookup"><span data-stu-id="73278-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="73278-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73278-187">-NatRuleCollection</span></span>
<span data-ttu-id="73278-188">Az AzureFirewallNatRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="73278-188">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="73278-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73278-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="73278-190">Az AzureFirewallNetworkRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="73278-190">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="73278-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="73278-191">-PrivateRange</span></span>
<span data-ttu-id="73278-192">A privát IP-tartományok, amelyekre a forgalom nem lesz SNAT-ed</span><span class="sxs-lookup"><span data-stu-id="73278-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="73278-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="73278-193">-PublicIpAddress</span></span>
<span data-ttu-id="73278-194">Egy vagy több nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="73278-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="73278-195">A nyilvános IP-címeknek szabványos termékváltozatot kell használniuk, és a tűzfallal azonos erőforráscsoporthoz kell tartozni.</span><span class="sxs-lookup"><span data-stu-id="73278-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="73278-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="73278-196">-PublicIpName</span></span>
<span data-ttu-id="73278-197">Nyilvános IP-név.</span><span class="sxs-lookup"><span data-stu-id="73278-197">Public Ip Name.</span></span> <span data-ttu-id="73278-198">A nyilvános IP-címnek szabványos termékváltozatot kell használnia, és ugyanannak az erőforráscsoportnak kell lennie, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="73278-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="73278-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73278-199">-ResourceGroupName</span></span>
<span data-ttu-id="73278-200">Annak az erőforráscsoportnak a nevét adja meg, amely tartalmazza a tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="73278-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="73278-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="73278-201">-SkuName</span></span>
<span data-ttu-id="73278-202">A tűzfal termékváltozatának neve</span><span class="sxs-lookup"><span data-stu-id="73278-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73278-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="73278-203">-SkuTier</span></span>
<span data-ttu-id="73278-204">A tűzfal termékváltozatrétege</span><span class="sxs-lookup"><span data-stu-id="73278-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73278-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="73278-205">-Tag</span></span>
<span data-ttu-id="73278-206">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="73278-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="73278-207">Például:</span><span class="sxs-lookup"><span data-stu-id="73278-207">For example:</span></span>

<span data-ttu-id="73278-208">@{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="73278-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="73278-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="73278-209">-ThreatIntelMode</span></span>
<span data-ttu-id="73278-210">A Veszélyforrás-felderítés üzemmódját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="73278-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="73278-211">Az alapértelmezett mód a Riasztás, nem pedig a Kikapcsolva.</span><span class="sxs-lookup"><span data-stu-id="73278-211">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="73278-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="73278-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="73278-213">The whitelist for Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="73278-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73278-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="73278-214">-VirtualHubId</span></span>
<span data-ttu-id="73278-215">A virtuális központ, amelyhez tűzfal van csatolva</span><span class="sxs-lookup"><span data-stu-id="73278-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73278-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73278-216">-VirtualNetwork</span></span>
<span data-ttu-id="73278-217">Virtual Network</span><span class="sxs-lookup"><span data-stu-id="73278-217">Virtual Network</span></span>

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

### <span data-ttu-id="73278-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="73278-218">-VirtualNetworkName</span></span>
<span data-ttu-id="73278-219">Annak a virtuális hálózatnak a neve, amelyre a tűzfalat telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="73278-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="73278-220">A virtuális hálózatnak és a tűzfalnak ugyanannak az erőforráscsoportnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="73278-220">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="73278-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="73278-221">-Zone</span></span>
<span data-ttu-id="73278-222">A rendelkezésre állási zónák listája, amely azt sorolja fel, hogy honnan kell a tűzfalnak létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="73278-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="73278-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73278-223">-Confirm</span></span>
<span data-ttu-id="73278-224">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="73278-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73278-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73278-225">-WhatIf</span></span>
<span data-ttu-id="73278-226">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="73278-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73278-227">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73278-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73278-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73278-228">CommonParameters</span></span>
<span data-ttu-id="73278-229">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73278-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73278-230">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73278-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73278-231">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73278-231">INPUTS</span></span>

### <span data-ttu-id="73278-232">System.String</span><span class="sxs-lookup"><span data-stu-id="73278-232">System.String</span></span>

### <span data-ttu-id="73278-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73278-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="73278-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="73278-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="73278-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="73278-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="73278-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="73278-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="73278-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="73278-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="73278-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="73278-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="73278-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="73278-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="73278-240">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73278-240">OUTPUTS</span></span>

### <span data-ttu-id="73278-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="73278-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="73278-242">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73278-242">NOTES</span></span>

## <span data-ttu-id="73278-243">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73278-243">RELATED LINKS</span></span>

[<span data-ttu-id="73278-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73278-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="73278-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73278-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="73278-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73278-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="73278-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73278-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="73278-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73278-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="73278-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73278-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
