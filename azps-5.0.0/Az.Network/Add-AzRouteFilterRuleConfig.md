---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195599"
---
# <span data-ttu-id="4affd-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4affd-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4affd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4affd-102">SYNOPSIS</span></span>
<span data-ttu-id="4affd-103">Az útvonal-szűrési szabály hozzáadása az útvonal-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="4affd-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="4affd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4affd-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4affd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4affd-105">DESCRIPTION</span></span>
<span data-ttu-id="4affd-106">Az Add-AzRouteFilterRuleConfig parancsmag egy útválasztási szűrési szabályt ad az Azure Route-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="4affd-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="4affd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4affd-107">EXAMPLES</span></span>

### <span data-ttu-id="4affd-108">1. példa: az útvonal-szűrési szabály hozzáadása az útvonal-szűrőhöz</span><span class="sxs-lookup"><span data-stu-id="4affd-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="4affd-109">Az első parancs az Get-AzRouteFilter parancsmag segítségével a routefilter01 nevű útvonalcsoport-szűrőt kapja.</span><span class="sxs-lookup"><span data-stu-id="4affd-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="4affd-110">A parancs a $RouteFilter változóban tárolja a szűrőt.</span><span class="sxs-lookup"><span data-stu-id="4affd-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="4affd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4affd-111">PARAMETERS</span></span>

### <span data-ttu-id="4affd-112">-Access</span><span class="sxs-lookup"><span data-stu-id="4affd-112">-Access</span></span>
<span data-ttu-id="4affd-113">Az útvonal-szűrő szabály elérését adja meg, az érvényes értékek megtagadják vagy engedélyezik.</span><span class="sxs-lookup"><span data-stu-id="4affd-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="4affd-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="4affd-114">-CommunityList</span></span>
<span data-ttu-id="4affd-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="4affd-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4affd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4affd-116">-DefaultProfile</span></span>
<span data-ttu-id="4affd-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4affd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4affd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4affd-118">-Force</span></span>
<span data-ttu-id="4affd-119">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4affd-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4affd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4affd-120">-Name</span></span>
<span data-ttu-id="4affd-121">Annak az útvonal-szűrő szabálynak a neve, amelyet az útvonal-szűrőhöz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="4affd-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="4affd-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-122">-RouteFilter</span></span>
<span data-ttu-id="4affd-123">Annak az útvonal-szűrőnek a meghatározása, amelyre a parancsmag az útvonal-szűrési szabályt hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="4affd-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="4affd-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="4affd-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="4affd-125">Az útvonal-szűrési szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4affd-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="4affd-126">Az érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="4affd-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="4affd-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4affd-127">-Confirm</span></span>
<span data-ttu-id="4affd-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4affd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4affd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4affd-129">-WhatIf</span></span>
<span data-ttu-id="4affd-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4affd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4affd-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4affd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4affd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4affd-132">CommonParameters</span></span>
<span data-ttu-id="4affd-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4affd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4affd-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4affd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4affd-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4affd-135">INPUTS</span></span>

### <span data-ttu-id="4affd-136">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4affd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4affd-137">OUTPUTS</span></span>

### <span data-ttu-id="4affd-138">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4affd-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4affd-139">NOTES</span></span>
<span data-ttu-id="4affd-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="4affd-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4affd-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4affd-141">RELATED LINKS</span></span>

[<span data-ttu-id="4affd-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4affd-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4affd-143">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4affd-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4affd-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4affd-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4affd-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4affd-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4affd-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4affd-147">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4affd-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4affd-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4affd-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)