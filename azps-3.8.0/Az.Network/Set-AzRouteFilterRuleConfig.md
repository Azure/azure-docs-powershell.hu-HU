---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013085"
---
# <span data-ttu-id="f99c2-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f99c2-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f99c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f99c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f99c2-103">Egy útvonal-szűrőhöz tartozó útvonaltervezés szabályának módosítása.</span><span class="sxs-lookup"><span data-stu-id="f99c2-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="f99c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f99c2-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f99c2-105">DESCRIPTION</span></span>
<span data-ttu-id="f99c2-106">A **set-AzRouteFilterRuleConfig** parancsmag módosította az útvonal-szűrő szabályát.</span><span class="sxs-lookup"><span data-stu-id="f99c2-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="f99c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f99c2-107">EXAMPLES</span></span>

### <span data-ttu-id="f99c2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f99c2-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="f99c2-109">Az első parancs megkapja a RouteFilter01 nevű útvonal-szűrőt, és a $rf változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f99c2-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="f99c2-110">A második parancs módosítja a Rule01 nevű útvonal-szűrő szabályát, és a $rf változóban frissíti az útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="f99c2-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="f99c2-111">A harmadik parancs a frissített útvonal szűrőt menti.</span><span class="sxs-lookup"><span data-stu-id="f99c2-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="f99c2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f99c2-112">PARAMETERS</span></span>

### <span data-ttu-id="f99c2-113">-Access</span><span class="sxs-lookup"><span data-stu-id="f99c2-113">-Access</span></span>
<span data-ttu-id="f99c2-114">A szabály hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="f99c2-114">The access type of the rule.</span></span>
<span data-ttu-id="f99c2-115">A lehetséges értékek a következők: "Allow", "deny"</span><span class="sxs-lookup"><span data-stu-id="f99c2-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="f99c2-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f99c2-116">-CommunityList</span></span>
<span data-ttu-id="f99c2-117">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="f99c2-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="f99c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99c2-118">-DefaultProfile</span></span>
<span data-ttu-id="f99c2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f99c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f99c2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f99c2-120">-Force</span></span>
<span data-ttu-id="f99c2-121">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f99c2-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f99c2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f99c2-122">-Name</span></span>
<span data-ttu-id="f99c2-123">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="f99c2-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="f99c2-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-124">-RouteFilter</span></span>
<span data-ttu-id="f99c2-125">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-125">The RouteFilter</span></span>

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

### <span data-ttu-id="f99c2-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f99c2-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="f99c2-127">Az útvonal-szűrő szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="f99c2-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="f99c2-128">Lehetséges értékek: "Közösség"</span><span class="sxs-lookup"><span data-stu-id="f99c2-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="f99c2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f99c2-129">-Confirm</span></span>
<span data-ttu-id="f99c2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f99c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99c2-131">-WhatIf</span></span>
<span data-ttu-id="f99c2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f99c2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f99c2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f99c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99c2-134">CommonParameters</span></span>
<span data-ttu-id="f99c2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f99c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99c2-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99c2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99c2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f99c2-137">INPUTS</span></span>

### <span data-ttu-id="f99c2-138">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f99c2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f99c2-139">OUTPUTS</span></span>

### <span data-ttu-id="f99c2-140">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f99c2-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f99c2-141">NOTES</span></span>

## <span data-ttu-id="f99c2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f99c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="f99c2-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f99c2-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f99c2-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f99c2-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f99c2-145">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f99c2-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f99c2-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f99c2-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f99c2-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f99c2-148">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f99c2-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="f99c2-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f99c2-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
