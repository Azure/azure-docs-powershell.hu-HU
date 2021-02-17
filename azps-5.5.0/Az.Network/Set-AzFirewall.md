---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156754"
---
# <span data-ttu-id="05829-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-101">Set-AzFirewall</span></span>

## <span data-ttu-id="05829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05829-102">SYNOPSIS</span></span>
<span data-ttu-id="05829-103">Módosított tűzfalat ment.</span><span class="sxs-lookup"><span data-stu-id="05829-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="05829-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05829-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05829-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05829-105">DESCRIPTION</span></span>
<span data-ttu-id="05829-106">A **Set-AzFirewall** parancsmag frissíti az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="05829-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="05829-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05829-107">EXAMPLES</span></span>

### <span data-ttu-id="05829-108">1: A tűzfal alkalmazásszabálycsoport prioritásának frissítése</span><span class="sxs-lookup"><span data-stu-id="05829-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="05829-109">Ez a példa frissíti egy Azure tűzfal meglévő szabálygyűjteményének prioritását.</span><span class="sxs-lookup"><span data-stu-id="05829-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="05829-110">Ha az "rg" erőforráscsoportban az Azure Firewall "AzureFirewall" egy "ruleCollectionName" nevű alkalmazásszabálygyűjteményt tartalmaz, a fenti parancsok megváltoztatják az adott szabálygyűjtemény prioritását, és később frissítik az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="05829-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="05829-111">A helyi Set-AzFirewall parancs nélkül a helyi objektumon $azFw műveletek nem jelennek meg a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="05829-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="05829-112">2: Azure tűzfal létrehozása és alkalmazásszabály-gyűjtemény beállítása később</span><span class="sxs-lookup"><span data-stu-id="05829-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="05829-113">Ebben a példában először egy tűzfal jön létre alkalmazásszabálygyűjtemények nélkül.</span><span class="sxs-lookup"><span data-stu-id="05829-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="05829-114">Ezután létrejön egy alkalmazásszabály és egy alkalmazásszabálygyűjtemény, majd a tűzfal objektum módosul a memóriában anélkül, hogy ez hatással lenne a felhőbeli valódi konfigurációra.</span><span class="sxs-lookup"><span data-stu-id="05829-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="05829-115">Ahhoz, hogy a módosítások a felhőben is tükröződni Set-AzFirewall meg kell őket.</span><span class="sxs-lookup"><span data-stu-id="05829-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="05829-116">3: A Threat Intel műveletmód frissítése az Azure tűzfalban</span><span class="sxs-lookup"><span data-stu-id="05829-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="05829-117">Ebben a példában az "rg" erőforráscsoportban az Azure Firewall "AzureFirewall" veszélyforrás-intel műveletmódját frissíti.</span><span class="sxs-lookup"><span data-stu-id="05829-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="05829-118">A helyi Set-AzFirewall parancs nélkül a helyi objektumon $azFw műveletek nem jelennek meg a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="05829-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="05829-119">4: A tűzfal áthelyezése és kiosztása</span><span class="sxs-lookup"><span data-stu-id="05829-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="05829-120">Ez a példa beolvassa a tűzfalat, áthelyezi a tűzfalat, és menti azt.</span><span class="sxs-lookup"><span data-stu-id="05829-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="05829-121">A Deallocate parancs eltávolítja a futó szolgáltatást, de megőrzi a tűzfal konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="05829-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="05829-122">Ahhoz, hogy a módosítások a felhőben is tükröződni Set-AzFirewall meg kell őket.</span><span class="sxs-lookup"><span data-stu-id="05829-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="05829-123">Ha a felhasználó ismét el szeretné kezdeni a szolgáltatást, a Tűzfalon meg kell hívatni a Kiosztás módszert.</span><span class="sxs-lookup"><span data-stu-id="05829-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="05829-124">Az új VNet és nyilvános IP-címnek ugyanabban az erőforráscsoportban kell lennie, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="05829-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="05829-125">Ahhoz, hogy a módosítások a felhőben is Set-AzFirewall meg.</span><span class="sxs-lookup"><span data-stu-id="05829-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="05829-126">5: Kiosztani egy felügyeleti nyilvános IP-címet a kényszerített átvezetési forgatókönyvekhez</span><span class="sxs-lookup"><span data-stu-id="05829-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="05829-127">Ez a példa kiosztja a tűzfalat egy felügyeleti nyilvános IP-címmel és alhálózattal a kényszerített átjárók esetén.</span><span class="sxs-lookup"><span data-stu-id="05829-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="05829-128">A VNetnek tartalmaznia kell egy "AzureFirewallManagementSubnet" nevű alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="05829-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="05829-129">6: Nyilvános IP-cím hozzáadása azure tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="05829-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="05829-130">Ebben a példában a tűzfalhoz csatolt "azFwPublicIp1" nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="05829-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="05829-131">7: Nyilvános IP-cím eltávolítása az Azure tűzfalról</span><span class="sxs-lookup"><span data-stu-id="05829-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="05829-132">Ebben a példában az "azFwPublicIp1" nyilvános IP-cím leválasztva a tűzfalról.</span><span class="sxs-lookup"><span data-stu-id="05829-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="05829-133">8: A felügyeleti nyilvános IP-cím módosítása az Azure tűzfalon</span><span class="sxs-lookup"><span data-stu-id="05829-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="05829-134">Ebben a példában a tűzfal felügyeleti nyilvános IP-címe "AzFwMgmtPublicIp2" lesz.</span><span class="sxs-lookup"><span data-stu-id="05829-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="05829-135">9: DNS-konfiguráció hozzáadása azure tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="05829-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="05829-136">Ebben a példában a DNS-proxy és a DNS-kiszolgáló konfigurációja a tűzfalhoz van csatolva.</span><span class="sxs-lookup"><span data-stu-id="05829-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="05829-137">10: Meglévő szabály célhelyének frissítése a tűzfal alkalmazásszabálygyűjteményében</span><span class="sxs-lookup"><span data-stu-id="05829-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="05829-138">Ez a példa frissíti egy meglévő szabály célhelyét egy Azure tűzfal szabálygyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="05829-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="05829-139">Ez lehetővé teszi, hogy automatikusan frissítse a szabályokat, amikor az IP-címek dinamikusan változnak.</span><span class="sxs-lookup"><span data-stu-id="05829-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="05829-140">11: Az Aktív FTP engedélyezése az Azure tűzfalon</span><span class="sxs-lookup"><span data-stu-id="05829-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="05829-141">Ebben a példában az Aktív FTP engedélyezve van a tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="05829-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="05829-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05829-142">PARAMETERS</span></span>

### <span data-ttu-id="05829-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05829-143">-AsJob</span></span>
<span data-ttu-id="05829-144">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="05829-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05829-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-145">-AzureFirewall</span></span>
<span data-ttu-id="05829-146">The AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="05829-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05829-147">-DefaultProfile</span></span>
<span data-ttu-id="05829-148">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05829-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05829-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05829-149">-Confirm</span></span>
<span data-ttu-id="05829-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05829-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05829-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05829-151">-WhatIf</span></span>
<span data-ttu-id="05829-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05829-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05829-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05829-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05829-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05829-154">CommonParameters</span></span>
<span data-ttu-id="05829-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05829-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05829-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05829-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05829-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05829-157">INPUTS</span></span>

### <span data-ttu-id="05829-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="05829-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05829-159">OUTPUTS</span></span>

### <span data-ttu-id="05829-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="05829-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05829-161">NOTES</span></span>

## <span data-ttu-id="05829-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05829-162">RELATED LINKS</span></span>

[<span data-ttu-id="05829-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="05829-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="05829-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05829-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
