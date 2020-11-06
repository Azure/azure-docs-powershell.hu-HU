---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501755"
---
# <span data-ttu-id="3a774-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a774-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="3a774-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a774-102">SYNOPSIS</span></span>
<span data-ttu-id="3a774-103">Az útvonal-szűrési szabály hozzáadása az útvonal-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="3a774-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a774-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a774-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a774-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a774-105">DESCRIPTION</span></span>
<span data-ttu-id="3a774-106">Az Add-AzureRmRouteFilterRuleConfig parancsmag egy útválasztási szűrési szabályt ad az Azure Route-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="3a774-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="3a774-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a774-107">EXAMPLES</span></span>

### <span data-ttu-id="3a774-108">--------------------------Példa 1: az útvonal-szűrési szabály hozzáadása az útvonal-szűrőhöz--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a774-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="3a774-109">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3a774-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="3a774-110">Az első parancs az Get-AzureRmRouteFilter parancsmag segítségével a routefilter01 nevű útvonalcsoport-szűrőt kapja.</span><span class="sxs-lookup"><span data-stu-id="3a774-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="3a774-111">A parancs a $RouteFilter változóban tárolja a szűrőt.</span><span class="sxs-lookup"><span data-stu-id="3a774-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="3a774-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a774-112">PARAMETERS</span></span>

### <span data-ttu-id="3a774-113">-Access</span><span class="sxs-lookup"><span data-stu-id="3a774-113">-Access</span></span>
<span data-ttu-id="3a774-114">Az útvonal-szűrő szabály elérését adja meg, az érvényes értékek megtagadják vagy engedélyezik.</span><span class="sxs-lookup"><span data-stu-id="3a774-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a774-115">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="3a774-115">-CommunityList</span></span>
<span data-ttu-id="3a774-116">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="3a774-116">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a774-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3a774-117">-Force</span></span>
<span data-ttu-id="3a774-118">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="3a774-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="3a774-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a774-119">-Name</span></span>
<span data-ttu-id="3a774-120">Annak az útvonal-szűrő szabálynak a neve, amelyet az útvonal-szűrőhöz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="3a774-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="3a774-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a774-121">-RouteFilter</span></span>
<span data-ttu-id="3a774-122">Annak az útvonal-szűrőnek a meghatározása, amelyre a parancsmag az útvonal-szűrési szabályt hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="3a774-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a774-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="3a774-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="3a774-124">Az útvonal-szűrési szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a774-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="3a774-125">Az érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="3a774-125">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a774-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3a774-126">-Confirm</span></span>
<span data-ttu-id="3a774-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a774-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a774-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a774-128">-WhatIf</span></span>
<span data-ttu-id="3a774-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3a774-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a774-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a774-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a774-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a774-131">-DefaultProfile</span></span>
<span data-ttu-id="3a774-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a774-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a774-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a774-133">CommonParameters</span></span>
<span data-ttu-id="3a774-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a774-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a774-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a774-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a774-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a774-136">INPUTS</span></span>

### <span data-ttu-id="3a774-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a774-137">PSRouteFilter</span></span>
<span data-ttu-id="3a774-138">A ' RouteFilter ' paraméter az "PSRouteFilter" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3a774-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="3a774-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a774-139">OUTPUTS</span></span>

### <span data-ttu-id="3a774-140">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a774-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3a774-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a774-141">NOTES</span></span>
<span data-ttu-id="3a774-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="3a774-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3a774-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a774-143">RELATED LINKS</span></span>

[<span data-ttu-id="3a774-144">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a774-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="3a774-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a774-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="3a774-146">Új – AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="3a774-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="3a774-147">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="3a774-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="3a774-148">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="3a774-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="3a774-149">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a774-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

