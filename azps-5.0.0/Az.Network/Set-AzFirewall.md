---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195330"
---
# <span data-ttu-id="39252-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-101">Set-AzFirewall</span></span>

## <span data-ttu-id="39252-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39252-102">SYNOPSIS</span></span>
<span data-ttu-id="39252-103">Módosított tűzfal mentése</span><span class="sxs-lookup"><span data-stu-id="39252-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="39252-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39252-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39252-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39252-105">DESCRIPTION</span></span>
<span data-ttu-id="39252-106">A **set-AzFirewall** parancsmag egy Azure-tűzfalat frissít.</span><span class="sxs-lookup"><span data-stu-id="39252-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="39252-107">Példák</span><span class="sxs-lookup"><span data-stu-id="39252-107">EXAMPLES</span></span>

### <span data-ttu-id="39252-108">1: a tűzfal-alkalmazási szabályok gyűjteményének frissítési prioritása</span><span class="sxs-lookup"><span data-stu-id="39252-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="39252-109">Ez a példa frissíti egy Azure-tűzfal meglévő szabálykészlet-gyűjteményének prioritását.</span><span class="sxs-lookup"><span data-stu-id="39252-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="39252-110">Feltételezve, hogy az Azure Firewall "AzureFirewall" az erőforráscsoport "RG" nevű ruleCollectionName tartalmaz, a fenti parancsok a szabály-gyűjtemény prioritását fogják módosítani, majd később frissítik az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="39252-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="39252-111">A Set-AzFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="39252-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="39252-112">2: Azure-tűzfal létrehozása és egy alkalmazási szabály gyűjteményének beállítása később</span><span class="sxs-lookup"><span data-stu-id="39252-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="39252-113">Ebben a példában a tűzfal először az alkalmazási szabályok gyűjteménye nélkül jön létre.</span><span class="sxs-lookup"><span data-stu-id="39252-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="39252-114">Ezt követően egy alkalmazási szabály és egy alkalmazási szabály gyűjtemény jön létre, a tűzfal objektum a memóriában módosul, és nem befolyásolja a Felhőbeli valós konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="39252-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="39252-115">Ha a változásokat a felhőben szeretné tükrözni, Set-AzFirewall kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="39252-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="39252-116">3: az Azure tűzfal Intel-üzemeltetési üzemmódjának frissítése</span><span class="sxs-lookup"><span data-stu-id="39252-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="39252-117">Ebben a példában a "RG" erőforráscsoport "AzureFirewall" az Azure Firewall "" veszélyforrást okozó Intel-üzemeltetési módot frissíti.</span><span class="sxs-lookup"><span data-stu-id="39252-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="39252-118">A Set-AzFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="39252-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="39252-119">4: a tűzfal felszabadítása és kiosztása</span><span class="sxs-lookup"><span data-stu-id="39252-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="39252-120">Ez a példa beolvassa a tűzfalat, felszabadítja a tűzfalat, és menti.</span><span class="sxs-lookup"><span data-stu-id="39252-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="39252-121">A kifoglalás parancs eltávolítja a futó szolgáltatást, de megőrzi a tűzfal konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="39252-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="39252-122">Ha a változásokat a felhőben szeretné tükrözni, Set-AzFirewall kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="39252-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="39252-123">Ha a felhasználó ismét el szeretné indítani a szolgáltatást, a kiosztási módszert a tűzfalon kell megneveznie.</span><span class="sxs-lookup"><span data-stu-id="39252-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="39252-124">Az új VNet és a nyilvános IP-nek ugyanabban az erőforráscsoport-csoportban kell lennie, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="39252-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="39252-125">A Felhőbeli módosítások esetében a Set-AzFirewallt is meg kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="39252-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="39252-126">5: a kezelés nyilvános IP-címének kiosztása kényszerített bújtatási forgatókönyvek esetén</span><span class="sxs-lookup"><span data-stu-id="39252-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="39252-127">Ez a példa kiosztja a tűzfalat egy felügyeleti nyilvános IP-címmel és alhálózattal kényszerített bújtatási forgatókönyvekhez.</span><span class="sxs-lookup"><span data-stu-id="39252-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="39252-128">A VNet tartalmaznia kell egy "AzureFirewallManagementSubnet" nevű alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="39252-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="39252-129">6: nyilvános IP-cím hozzáadása Azure-tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="39252-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="39252-130">Ebben a példában az "azFwPublicIp1" nyilvános IP-cím a tűzfalhoz van csatolva.</span><span class="sxs-lookup"><span data-stu-id="39252-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="39252-131">7: nyilvános IP-cím eltávolítása Azure-tűzfalról</span><span class="sxs-lookup"><span data-stu-id="39252-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="39252-132">Ebben a példában a "azFwPublicIp1" nyilvános IP-cím le van távolítva a tűzfalról.</span><span class="sxs-lookup"><span data-stu-id="39252-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="39252-133">8: az irányítás nyilvános IP-címének módosítása Azure tűzfalon</span><span class="sxs-lookup"><span data-stu-id="39252-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="39252-134">Ebben a példában a tűzfal nyilvános IP-címe a következőre változik: "AzFwMgmtPublicIp2".</span><span class="sxs-lookup"><span data-stu-id="39252-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="39252-135">9: DNS-konfiguráció hozzáadása Azure-tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="39252-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="39252-136">Ebben a példában a rendszer a tűzfalhoz csatolja a DNS-proxyt és a DNS-kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="39252-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="39252-137">10: egy meglévő szabály célhelyének frissítése a tűzfal alkalmazási szabály-gyűjteményben</span><span class="sxs-lookup"><span data-stu-id="39252-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="39252-138">Ez a példa frissíti egy meglévő szabály rendeltetését az Azure-tűzfalban lévő szabályok gyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="39252-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="39252-139">Ezzel a beállítással automatikusan frissítheti a szabályokat, ha az IP-címek dinamikusan változnak.</span><span class="sxs-lookup"><span data-stu-id="39252-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="39252-140">11: az aktív FTP engedélyezése az Azure tűzfalon</span><span class="sxs-lookup"><span data-stu-id="39252-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="39252-141">Ebben a példában az aktív FTP engedélyezve van a tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="39252-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="39252-142">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39252-142">PARAMETERS</span></span>

### <span data-ttu-id="39252-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39252-143">-AsJob</span></span>
<span data-ttu-id="39252-144">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="39252-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39252-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-145">-AzureFirewall</span></span>
<span data-ttu-id="39252-146">A AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39252-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39252-147">-DefaultProfile</span></span>
<span data-ttu-id="39252-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39252-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39252-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39252-149">-Confirm</span></span>
<span data-ttu-id="39252-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39252-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39252-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39252-151">-WhatIf</span></span>
<span data-ttu-id="39252-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39252-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39252-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39252-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39252-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39252-154">CommonParameters</span></span>
<span data-ttu-id="39252-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39252-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39252-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39252-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39252-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39252-157">INPUTS</span></span>

### <span data-ttu-id="39252-158">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="39252-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39252-159">OUTPUTS</span></span>

### <span data-ttu-id="39252-160">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="39252-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39252-161">NOTES</span></span>

## <span data-ttu-id="39252-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39252-162">RELATED LINKS</span></span>

[<span data-ttu-id="39252-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="39252-164">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="39252-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="39252-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
