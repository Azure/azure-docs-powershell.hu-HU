---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670014"
---
# <span data-ttu-id="77c1f-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-101">Set-AzFirewall</span></span>

## <span data-ttu-id="77c1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="77c1f-103">Módosított tűzfal mentése</span><span class="sxs-lookup"><span data-stu-id="77c1f-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="77c1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77c1f-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77c1f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="77c1f-106">A **set-AzFirewall** parancsmag egy Azure-tűzfalat frissít.</span><span class="sxs-lookup"><span data-stu-id="77c1f-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="77c1f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="77c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="77c1f-108">1: a tűzfal-alkalmazási szabályok gyűjteményének frissítési prioritása</span><span class="sxs-lookup"><span data-stu-id="77c1f-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="77c1f-109">Ez a példa frissíti egy Azure-tűzfal meglévő szabálykészlet-gyűjteményének prioritását.</span><span class="sxs-lookup"><span data-stu-id="77c1f-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="77c1f-110">Feltételezve, hogy az Azure Firewall "AzureFirewall" az erőforráscsoport "RG" nevű ruleCollectionName tartalmaz, a fenti parancsok a szabály-gyűjtemény prioritását fogják módosítani, majd később frissítik az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="77c1f-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="77c1f-111">A Set-AzFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="77c1f-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="77c1f-112">2: Azure-tűzfal létrehozása és egy alkalmazási szabály gyűjteményének beállítása később</span><span class="sxs-lookup"><span data-stu-id="77c1f-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="77c1f-113">Ebben a példában a tűzfal először az alkalmazási szabályok gyűjteménye nélkül jön létre.</span><span class="sxs-lookup"><span data-stu-id="77c1f-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="77c1f-114">Ezt követően egy alkalmazási szabály és egy alkalmazási szabály gyűjtemény jön létre, a tűzfal objektum a memóriában módosul, és nem befolyásolja a Felhőbeli valós konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="77c1f-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="77c1f-115">Ha a változásokat a felhőben szeretné tükrözni, Set-AzFirewall kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="77c1f-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="77c1f-116">3: az Azure tűzfal Intel-üzemeltetési üzemmódjának frissítése</span><span class="sxs-lookup"><span data-stu-id="77c1f-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="77c1f-117">Ebben a példában a "RG" erőforráscsoport "AzureFirewall" az Azure Firewall "" veszélyforrást okozó Intel-üzemeltetési módot frissíti.</span><span class="sxs-lookup"><span data-stu-id="77c1f-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="77c1f-118">A Set-AzFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="77c1f-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="77c1f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77c1f-119">PARAMETERS</span></span>

### <span data-ttu-id="77c1f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77c1f-120">-AsJob</span></span>
<span data-ttu-id="77c1f-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="77c1f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77c1f-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-122">-AzureFirewall</span></span>
<span data-ttu-id="77c1f-123">A AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-123">The AzureFirewall</span></span>

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

### <span data-ttu-id="77c1f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c1f-124">-DefaultProfile</span></span>
<span data-ttu-id="77c1f-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77c1f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77c1f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77c1f-126">-Confirm</span></span>
<span data-ttu-id="77c1f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77c1f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c1f-128">-WhatIf</span></span>
<span data-ttu-id="77c1f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77c1f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77c1f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77c1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c1f-131">CommonParameters</span></span>
<span data-ttu-id="77c1f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77c1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c1f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c1f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c1f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77c1f-134">INPUTS</span></span>

### <span data-ttu-id="77c1f-135">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="77c1f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77c1f-136">OUTPUTS</span></span>

### <span data-ttu-id="77c1f-137">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="77c1f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77c1f-138">NOTES</span></span>

## <span data-ttu-id="77c1f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77c1f-139">RELATED LINKS</span></span>

[<span data-ttu-id="77c1f-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="77c1f-141">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="77c1f-142">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="77c1f-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
