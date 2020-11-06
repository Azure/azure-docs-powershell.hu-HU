---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491907"
---
# <span data-ttu-id="6c3a9-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="6c3a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3a9-103">Módosított tűzfal mentése</span><span class="sxs-lookup"><span data-stu-id="6c3a9-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c3a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c3a9-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c3a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c3a9-105">DESCRIPTION</span></span>
<span data-ttu-id="6c3a9-106">A **set-AzureRmFirewall** parancsmag egy Azure-tűzfalat frissít.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="6c3a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6c3a9-107">EXAMPLES</span></span>

### <span data-ttu-id="6c3a9-108">1: a tűzfal-alkalmazási szabályok gyűjteményének frissítési prioritása</span><span class="sxs-lookup"><span data-stu-id="6c3a9-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="6c3a9-109">Ez a példa frissíti egy Azure-tűzfal meglévő szabálykészlet-gyűjteményének prioritását.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="6c3a9-110">Feltételezve, hogy az Azure Firewall "AzureFirewall" az erőforráscsoport "RG" nevű ruleCollectionName tartalmaz, a fenti parancsok a szabály-gyűjtemény prioritását fogják módosítani, majd később frissítik az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="6c3a9-111">A Set-AzureRmFirewall parancs nélkül a helyi $azFw-objektumon végrehajtott összes művelet nem tükröződik a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="6c3a9-112">2: Azure-tűzfal létrehozása és egy alkalmazási szabály gyűjteményének beállítása később</span><span class="sxs-lookup"><span data-stu-id="6c3a9-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="6c3a9-113">Ebben a példában a tűzfal először az alkalmazási szabályok gyűjteménye nélkül jön létre.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="6c3a9-114">Ezt követően egy alkalmazási szabály és egy alkalmazási szabály gyűjtemény jön létre, a tűzfal objektum a memóriában módosul, és nem befolyásolja a Felhőbeli valós konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="6c3a9-115">Ha a változásokat a felhőben szeretné tükrözni, Set-AzureRmFirewall kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="6c3a9-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c3a9-116">PARAMETERS</span></span>

### <span data-ttu-id="6c3a9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c3a9-117">-AsJob</span></span>
<span data-ttu-id="6c3a9-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6c3a9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c3a9-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-119">-AzureFirewall</span></span>
<span data-ttu-id="6c3a9-120">A AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c3a9-121">-DefaultProfile</span></span>
<span data-ttu-id="6c3a9-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3a9-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c3a9-123">-Confirm</span></span>
<span data-ttu-id="6c3a9-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c3a9-125">-WhatIf</span></span>
<span data-ttu-id="6c3a9-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c3a9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c3a9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3a9-128">CommonParameters</span></span>
<span data-ttu-id="6c3a9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c3a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3a9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c3a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3a9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c3a9-131">INPUTS</span></span>

### <span data-ttu-id="6c3a9-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-132">PSAzureFirewall</span></span>
<span data-ttu-id="6c3a9-133">A ' AzureFirewall ' paraméter az "PSAzureFirewall" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6c3a9-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="6c3a9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c3a9-134">OUTPUTS</span></span>

### <span data-ttu-id="6c3a9-135">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="6c3a9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c3a9-136">NOTES</span></span>

## <span data-ttu-id="6c3a9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c3a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="6c3a9-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="6c3a9-139">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="6c3a9-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6c3a9-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
