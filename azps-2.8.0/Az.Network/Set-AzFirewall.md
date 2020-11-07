---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 6d0935b0b2c5296a5d45d25c56cd7feb9e269a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837023"
---
# <span data-ttu-id="e8fd1-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-101">Set-AzFirewall</span></span>

## <span data-ttu-id="e8fd1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fd1-103">Módosított tűzfal mentése</span><span class="sxs-lookup"><span data-stu-id="e8fd1-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="e8fd1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8fd1-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8fd1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="e8fd1-106">A **set-AzFirewall** parancsmag egy Azure-tűzfalat frissít.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="e8fd1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e8fd1-107">EXAMPLES</span></span>

### <span data-ttu-id="e8fd1-108">1: a tűzfal-alkalmazási szabályok gyűjteményének frissítési prioritása</span><span class="sxs-lookup"><span data-stu-id="e8fd1-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="e8fd1-109">Ez a példa frissíti egy Azure-tűzfal meglévő szabálykészlet-gyűjteményének prioritását.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="e8fd1-110">Feltételezve, hogy az Azure Firewall "AzureFirewall" az erőforráscsoport "RG" nevű ruleCollectionName tartalmaz, a fenti parancsok a szabály-gyűjtemény prioritását fogják módosítani, majd később frissítik az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="e8fd1-111">A Set-AzFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="e8fd1-112">2: Azure-tűzfal létrehozása és egy alkalmazási szabály gyűjteményének beállítása később</span><span class="sxs-lookup"><span data-stu-id="e8fd1-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="e8fd1-113">Ebben a példában a tűzfal először az alkalmazási szabályok gyűjteménye nélkül jön létre.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="e8fd1-114">Ezt követően egy alkalmazási szabály és egy alkalmazási szabály gyűjtemény jön létre, a tűzfal objektum a memóriában módosul, és nem befolyásolja a Felhőbeli valós konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="e8fd1-115">Ha a változásokat a felhőben szeretné tükrözni, Set-AzFirewall kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="e8fd1-116">3: az Azure tűzfal Intel-üzemeltetési üzemmódjának frissítése</span><span class="sxs-lookup"><span data-stu-id="e8fd1-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="e8fd1-117">Ebben a példában a "RG" erőforráscsoport "AzureFirewall" az Azure Firewall "" veszélyforrást okozó Intel-üzemeltetési módot frissíti.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="e8fd1-118">A Set-AzFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="e8fd1-119">4: a tűzfal felszabadítása és kiosztása</span><span class="sxs-lookup"><span data-stu-id="e8fd1-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```

<span data-ttu-id="e8fd1-120">Ez a példa beolvassa a tűzfalat, felszabadítja a tűzfalat, és menti.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="e8fd1-121">A kifoglalás parancs eltávolítja a futó szolgáltatást, de megőrzi a tűzfal konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="e8fd1-122">Ha a változásokat a felhőben szeretné tükrözni, Set-AzFirewall kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="e8fd1-123">Ha a felhasználó ismét el szeretné indítani a szolgáltatást, a kiosztási módszert a tűzfalon kell megneveznie.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="e8fd1-124">Az új VNet és a nyilvános IP-nek ugyanabban az erőforráscsoport-csoportban kell lennie, mint a tűzfal.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="e8fd1-125">A Felhőbeli módosítások esetében a Set-AzFirewallt is meg kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="e8fd1-126">5: nyilvános IP-cím hozzáadása Azure-tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="e8fd1-126">5:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="e8fd1-127">Ebben a példában az "azFwPublicIp1" nyilvános IP-cím a tűzfalhoz van csatolva.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-127">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="e8fd1-128">6: nyilvános IP-cím eltávolítása Azure-tűzfalról</span><span class="sxs-lookup"><span data-stu-id="e8fd1-128">6:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="e8fd1-129">Ebben a példában a "azFwPublicIp1" nyilvános IP-cím le van távolítva a tűzfalról.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-129">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

## <span data-ttu-id="e8fd1-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8fd1-130">PARAMETERS</span></span>

### <span data-ttu-id="e8fd1-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8fd1-131">-AsJob</span></span>
<span data-ttu-id="e8fd1-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e8fd1-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8fd1-133">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-133">-AzureFirewall</span></span>
<span data-ttu-id="e8fd1-134">A AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-134">The AzureFirewall</span></span>

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

### <span data-ttu-id="e8fd1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8fd1-135">-DefaultProfile</span></span>
<span data-ttu-id="e8fd1-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8fd1-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8fd1-137">-Confirm</span></span>
<span data-ttu-id="e8fd1-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8fd1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8fd1-139">-WhatIf</span></span>
<span data-ttu-id="e8fd1-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8fd1-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8fd1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fd1-142">CommonParameters</span></span>
<span data-ttu-id="e8fd1-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8fd1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fd1-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8fd1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fd1-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8fd1-145">INPUTS</span></span>

### <span data-ttu-id="e8fd1-146">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e8fd1-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8fd1-147">OUTPUTS</span></span>

### <span data-ttu-id="e8fd1-148">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e8fd1-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8fd1-149">NOTES</span></span>

## <span data-ttu-id="e8fd1-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8fd1-150">RELATED LINKS</span></span>

[<span data-ttu-id="e8fd1-151">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-151">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="e8fd1-152">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e8fd1-153">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e8fd1-153">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
