---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181534"
---
# <span data-ttu-id="225dd-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="225dd-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="225dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="225dd-102">SYNOPSIS</span></span>
<span data-ttu-id="225dd-103">Az útvonal-szűrő szabályait távolítja el az útvonal-szűrőből.</span><span class="sxs-lookup"><span data-stu-id="225dd-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="225dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="225dd-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="225dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="225dd-105">DESCRIPTION</span></span>
<span data-ttu-id="225dd-106">A **Remove-AzRouteFilterRuleConfig** parancsmag az útvonaltervezés szabályait távolítja el az útvonal szűrőből.</span><span class="sxs-lookup"><span data-stu-id="225dd-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="225dd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="225dd-107">EXAMPLES</span></span>

### <span data-ttu-id="225dd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="225dd-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="225dd-109">Az első parancs beolvassa a RouteFilter01 nevű ResourceGroup01 nevű szűrőt, amely a nevű erőforráscsoporthoz tartozik, és a $rf változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="225dd-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="225dd-110">A második parancs eltávolítja a Rule01 nevű útvonal-szűrő szabályt az $rf tárolt útvonal-szűrőből.</span><span class="sxs-lookup"><span data-stu-id="225dd-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="225dd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="225dd-111">PARAMETERS</span></span>

### <span data-ttu-id="225dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225dd-112">-DefaultProfile</span></span>
<span data-ttu-id="225dd-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="225dd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="225dd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="225dd-114">-Force</span></span>
<span data-ttu-id="225dd-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="225dd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="225dd-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="225dd-116">-Name</span></span>
<span data-ttu-id="225dd-117">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="225dd-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="225dd-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-118">-RouteFilter</span></span>
<span data-ttu-id="225dd-119">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-119">The RouteFilter</span></span>

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

### <span data-ttu-id="225dd-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="225dd-120">-Confirm</span></span>
<span data-ttu-id="225dd-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="225dd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225dd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225dd-122">-WhatIf</span></span>
<span data-ttu-id="225dd-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="225dd-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="225dd-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="225dd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225dd-125">CommonParameters</span></span>
<span data-ttu-id="225dd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="225dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225dd-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225dd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225dd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="225dd-128">INPUTS</span></span>

### <span data-ttu-id="225dd-129">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="225dd-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="225dd-130">OUTPUTS</span></span>

### <span data-ttu-id="225dd-131">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="225dd-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="225dd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="225dd-132">NOTES</span></span>

## <span data-ttu-id="225dd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="225dd-133">RELATED LINKS</span></span>

[<span data-ttu-id="225dd-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="225dd-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="225dd-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="225dd-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="225dd-136">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="225dd-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="225dd-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="225dd-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="225dd-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="225dd-139">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="225dd-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="225dd-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="225dd-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
