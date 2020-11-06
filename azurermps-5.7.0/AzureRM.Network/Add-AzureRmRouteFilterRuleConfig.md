---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 5daf0c5f764a095906e31167d6ddbc764ae68d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499788"
---
# <span data-ttu-id="8adfa-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8adfa-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8adfa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8adfa-102">SYNOPSIS</span></span>
<span data-ttu-id="8adfa-103">Az útvonal-szűrési szabály hozzáadása az útvonal-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="8adfa-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8adfa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8adfa-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8adfa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8adfa-105">DESCRIPTION</span></span>
<span data-ttu-id="8adfa-106">Az Add-AzureRmRouteFilterRuleConfig parancsmag egy útválasztási szűrési szabályt ad az Azure Route-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="8adfa-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="8adfa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8adfa-107">EXAMPLES</span></span>

### <span data-ttu-id="8adfa-108">--------------------------Példa 1: az útvonal-szűrési szabály hozzáadása az útvonal-szűrőhöz--------------------------</span><span class="sxs-lookup"><span data-stu-id="8adfa-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="8adfa-109">Az első parancs az Get-AzureRmRouteFilter parancsmag segítségével a routefilter01 nevű útvonalcsoport-szűrőt kapja.</span><span class="sxs-lookup"><span data-stu-id="8adfa-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="8adfa-110">A parancs a $RouteFilter változóban tárolja a szűrőt.</span><span class="sxs-lookup"><span data-stu-id="8adfa-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="8adfa-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8adfa-111">PARAMETERS</span></span>

### <span data-ttu-id="8adfa-112">-Access</span><span class="sxs-lookup"><span data-stu-id="8adfa-112">-Access</span></span>
<span data-ttu-id="8adfa-113">Az útvonal-szűrő szabály elérését adja meg, az érvényes értékek megtagadják vagy engedélyezik.</span><span class="sxs-lookup"><span data-stu-id="8adfa-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adfa-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="8adfa-114">-CommunityList</span></span>
<span data-ttu-id="8adfa-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="8adfa-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="8adfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8adfa-116">-DefaultProfile</span></span>
<span data-ttu-id="8adfa-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8adfa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8adfa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8adfa-118">-Force</span></span>
<span data-ttu-id="8adfa-119">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="8adfa-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8adfa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8adfa-120">-Name</span></span>
<span data-ttu-id="8adfa-121">Annak az útvonal-szűrő szabálynak a neve, amelyet az útvonal-szűrőhöz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="8adfa-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adfa-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8adfa-122">-RouteFilter</span></span>
<span data-ttu-id="8adfa-123">Annak az útvonal-szűrőnek a meghatározása, amelyre a parancsmag az útvonal-szűrési szabályt hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="8adfa-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8adfa-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="8adfa-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="8adfa-125">Az útvonal-szűrési szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8adfa-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="8adfa-126">Az érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="8adfa-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adfa-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8adfa-127">-Confirm</span></span>
<span data-ttu-id="8adfa-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8adfa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8adfa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8adfa-129">-WhatIf</span></span>
<span data-ttu-id="8adfa-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8adfa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8adfa-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8adfa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8adfa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8adfa-132">CommonParameters</span></span>
<span data-ttu-id="8adfa-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8adfa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8adfa-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8adfa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8adfa-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8adfa-135">INPUTS</span></span>

### <span data-ttu-id="8adfa-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8adfa-136">PSRouteFilter</span></span>
<span data-ttu-id="8adfa-137">A ' RouteFilter ' paraméter az "PSRouteFilter" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8adfa-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="8adfa-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8adfa-138">OUTPUTS</span></span>

### <span data-ttu-id="8adfa-139">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8adfa-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8adfa-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8adfa-140">NOTES</span></span>
<span data-ttu-id="8adfa-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="8adfa-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8adfa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8adfa-142">RELATED LINKS</span></span>

[<span data-ttu-id="8adfa-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8adfa-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8adfa-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8adfa-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="8adfa-145">Új – AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="8adfa-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="8adfa-146">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="8adfa-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="8adfa-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="8adfa-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="8adfa-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8adfa-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

