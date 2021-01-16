---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341681"
---
# <span data-ttu-id="a165e-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a165e-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="a165e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a165e-102">SYNOPSIS</span></span>
<span data-ttu-id="a165e-103">Útvonalszűrő szabályt ad hozzá az útvonalszűrőkhez.</span><span class="sxs-lookup"><span data-stu-id="a165e-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="a165e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a165e-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a165e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a165e-105">DESCRIPTION</span></span>
<span data-ttu-id="a165e-106">A Add-AzRouteFilterRuleConfig parancsmag hozzáad egy útvonalszűrő szabályt egy Azure-útvonalszűrőhez.</span><span class="sxs-lookup"><span data-stu-id="a165e-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="a165e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a165e-107">EXAMPLES</span></span>

### <span data-ttu-id="a165e-108">1. példa: Útvonalszűrő szabály hozzáadása útvonalszűrőhez</span><span class="sxs-lookup"><span data-stu-id="a165e-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="a165e-109">Az első parancs egy routefilter01 nevű útvonalszűrőt kap a Get-AzRouteFilter parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a165e-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="a165e-110">A parancs a szűrőt a $RouteFilter tárolja.</span><span class="sxs-lookup"><span data-stu-id="a165e-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="a165e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a165e-111">PARAMETERS</span></span>

### <span data-ttu-id="a165e-112">-Access</span><span class="sxs-lookup"><span data-stu-id="a165e-112">-Access</span></span>
<span data-ttu-id="a165e-113">Az útvonalszűrő-szabály hozzáférését adja meg, érvényes értékek: Elutasítás vagy Megengedve.</span><span class="sxs-lookup"><span data-stu-id="a165e-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="a165e-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="a165e-114">-CommunityList</span></span>
<span data-ttu-id="a165e-115">Az útvonalszűrőt szűrő közösségi értékek listája</span><span class="sxs-lookup"><span data-stu-id="a165e-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="a165e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a165e-116">-DefaultProfile</span></span>
<span data-ttu-id="a165e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a165e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a165e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a165e-118">-Force</span></span>
<span data-ttu-id="a165e-119">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="a165e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a165e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a165e-120">-Name</span></span>
<span data-ttu-id="a165e-121">Megadja annak az útvonalszűrő-szabálynak a nevét, amit hozzá szeretne adni az útvonalszűrőhez.</span><span class="sxs-lookup"><span data-stu-id="a165e-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="a165e-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-122">-RouteFilter</span></span>
<span data-ttu-id="a165e-123">Megadja azt az útvonalszűrőt, amelyhez ez a parancsmag útvonalszűrő szabályt ad.</span><span class="sxs-lookup"><span data-stu-id="a165e-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="a165e-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="a165e-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="a165e-125">Az útvonalszűrő-szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a165e-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="a165e-126">Érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="a165e-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="a165e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a165e-127">-Confirm</span></span>
<span data-ttu-id="a165e-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a165e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a165e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a165e-129">-WhatIf</span></span>
<span data-ttu-id="a165e-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a165e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a165e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a165e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a165e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a165e-132">CommonParameters</span></span>
<span data-ttu-id="a165e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a165e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a165e-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a165e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a165e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a165e-135">INPUTS</span></span>

### <span data-ttu-id="a165e-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a165e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a165e-137">OUTPUTS</span></span>

### <span data-ttu-id="a165e-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a165e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a165e-139">NOTES</span></span>
<span data-ttu-id="a165e-140">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="a165e-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a165e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a165e-141">RELATED LINKS</span></span>

[<span data-ttu-id="a165e-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a165e-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a165e-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a165e-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a165e-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a165e-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a165e-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a165e-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a165e-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="a165e-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="a165e-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="a165e-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a165e-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
