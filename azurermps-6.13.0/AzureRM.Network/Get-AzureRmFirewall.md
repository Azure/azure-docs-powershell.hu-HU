---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680329"
---
# <span data-ttu-id="37d34-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37d34-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="37d34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37d34-102">SYNOPSIS</span></span>
<span data-ttu-id="37d34-103">Azure-tűzfalat kap.</span><span class="sxs-lookup"><span data-stu-id="37d34-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37d34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37d34-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37d34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37d34-105">DESCRIPTION</span></span>
<span data-ttu-id="37d34-106">A **Get-AzureRmFirewall** parancsmag egy vagy több tűzfalat kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="37d34-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="37d34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37d34-107">EXAMPLES</span></span>

### <span data-ttu-id="37d34-108">1: az összes tűzfal lekérése egy erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="37d34-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="37d34-109">Ebben a példában a "rgName" erőforráscsoporthoz tartozó összes tűzfalat beolvassa.</span><span class="sxs-lookup"><span data-stu-id="37d34-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="37d34-110">2: tűzfal beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="37d34-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="37d34-111">Ez a példa a "azFw" nevű tűzfalat olvassa be a "rgName" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="37d34-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="37d34-112">3: a tűzfal lekérése, majd az alkalmazási szabályok gyűjteményének hozzáadása a tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="37d34-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="37d34-113">Ez a példa beolvassa a tűzfalat, majd felvesz egy alkalmazási szabályt a tűzfalba a hívási mód AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="37d34-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="37d34-114">4: a tűzfal lekérése, majd a hálózati szabályok gyűjteményének hozzáadása a tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="37d34-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="37d34-115">Ez a példa beolvassa a tűzfalat, majd egy hálózati szabály gyűjteményt ad a tűzfalhoz a hívási mód AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="37d34-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="37d34-116">5: a tűzfal lekérése, majd egy alkalmazási szabály gyűjteményének beolvasása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="37d34-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="37d34-117">Ez a példa beolvassa a tűzfalat, és a GetApplicationRuleCollectionByName a tűzfal objektumon név szerint begyűjti a szabályok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="37d34-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37d34-118">A szabály GetApplicationRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="37d34-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37d34-119">6: a tűzfal lekérése, majd egy hálózati szabály-gyűjtemény beolvasása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="37d34-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="37d34-120">Ez a példa beolvassa a tűzfalat, és a GetNetworkRuleCollectionByName a tűzfal objektumon név szerint begyűjti a szabályok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="37d34-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37d34-121">A szabály GetNetworkRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="37d34-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37d34-122">7: a tűzfal lekérése, majd az alkalmazás szabály-gyűjteményének eltávolítása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="37d34-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="37d34-123">Ez a példa beolvassa a tűzfalat, majd eltávolítja a szabályok gyűjteményét név szerint, a hívási mód RemoveApplicationRuleCollectionByName a tűzfal objektumon.</span><span class="sxs-lookup"><span data-stu-id="37d34-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37d34-124">A szabály RemoveApplicationRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="37d34-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37d34-125">8: a tűzfal lekérése, majd egy hálózati szabály-gyűjtemény eltávolítása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="37d34-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="37d34-126">Ez a példa beolvassa a tűzfalat, majd eltávolítja a szabályok gyűjteményét név szerint, a hívási mód RemoveNetworkRuleCollectionByName a tűzfal objektumon.</span><span class="sxs-lookup"><span data-stu-id="37d34-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37d34-127">A szabály RemoveNetworkRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="37d34-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37d34-128">9: a tűzfal lekérése, majd a tűzfal lefoglalása</span><span class="sxs-lookup"><span data-stu-id="37d34-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="37d34-129">Ebben a példában egy tűzfal és a hívások lefoglalása a tűzfalon a tűzfalhoz társított konfiguráció (alkalmazás és hálózati szabály gyűjtemény) segítségével indítható el.</span><span class="sxs-lookup"><span data-stu-id="37d34-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="37d34-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37d34-130">PARAMETERS</span></span>

### <span data-ttu-id="37d34-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d34-131">-DefaultProfile</span></span>
<span data-ttu-id="37d34-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37d34-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37d34-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37d34-133">-Name</span></span>
<span data-ttu-id="37d34-134">Annak a tűzfalnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="37d34-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d34-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d34-135">-ResourceGroupName</span></span>
<span data-ttu-id="37d34-136">Annak a csoportnak a neve, amelyhez a tűzfal tartozik.</span><span class="sxs-lookup"><span data-stu-id="37d34-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="37d34-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d34-137">CommonParameters</span></span>
<span data-ttu-id="37d34-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37d34-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d34-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d34-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d34-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37d34-140">INPUTS</span></span>

### <span data-ttu-id="37d34-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="37d34-141">None</span></span>
<span data-ttu-id="37d34-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="37d34-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37d34-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37d34-143">OUTPUTS</span></span>

### <span data-ttu-id="37d34-144">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="37d34-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="37d34-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37d34-145">NOTES</span></span>

## <span data-ttu-id="37d34-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37d34-146">RELATED LINKS</span></span>

[<span data-ttu-id="37d34-147">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37d34-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="37d34-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37d34-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="37d34-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37d34-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
