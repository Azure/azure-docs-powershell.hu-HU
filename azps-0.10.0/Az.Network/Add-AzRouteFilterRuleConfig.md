---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: ded23a30c078cd1d474310d73d94717d050f6824
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399277"
---
# <span data-ttu-id="122c5-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="122c5-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="122c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="122c5-102">SYNOPSIS</span></span>
<span data-ttu-id="122c5-103">Útvonalszűrő szabályt ad hozzá egy útvonalszűrőhez.</span><span class="sxs-lookup"><span data-stu-id="122c5-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="122c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="122c5-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="122c5-105">DESCRIPTION</span></span>
<span data-ttu-id="122c5-106">A Add-AzRouteFilterRuleConfig parancsmag hozzáad egy útvonalszűrő szabályt egy Azure-útvonalszűrőhez.</span><span class="sxs-lookup"><span data-stu-id="122c5-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="122c5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="122c5-107">EXAMPLES</span></span>

### <span data-ttu-id="122c5-108">-------------------------- 1. példa: Útvonalszűrő szabály hozzáadása útvonalszűrő---------------------------</span><span class="sxs-lookup"><span data-stu-id="122c5-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="122c5-109">Az első parancs egy routefilter01 nevű útvonalszűrőt kap a Get-AzRouteFilter parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="122c5-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="122c5-110">A parancs a szűrőt a $RouteFilter tárolja.</span><span class="sxs-lookup"><span data-stu-id="122c5-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="122c5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="122c5-111">PARAMETERS</span></span>

### <span data-ttu-id="122c5-112">-Access</span><span class="sxs-lookup"><span data-stu-id="122c5-112">-Access</span></span>
<span data-ttu-id="122c5-113">Az útvonalszűrő szabály hozzáférését adja meg, érvényes értékek: Elutasítás vagy Megengedve.</span><span class="sxs-lookup"><span data-stu-id="122c5-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="122c5-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="122c5-114">-CommunityList</span></span>
<span data-ttu-id="122c5-115">Az útvonalszűrőt szűrő közösségi értékek listája</span><span class="sxs-lookup"><span data-stu-id="122c5-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="122c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122c5-116">-DefaultProfile</span></span>
<span data-ttu-id="122c5-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="122c5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="122c5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="122c5-118">-Force</span></span>
<span data-ttu-id="122c5-119">Ne kérjen megerősítést, ha szeretné felülírni az erőforrást</span><span class="sxs-lookup"><span data-stu-id="122c5-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="122c5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="122c5-120">-Name</span></span>
<span data-ttu-id="122c5-121">Megadja annak az útvonalszűrő-szabálynak a nevét, amit hozzá szeretne adni az útvonalszűrőhez.</span><span class="sxs-lookup"><span data-stu-id="122c5-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="122c5-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="122c5-122">-RouteFilter</span></span>
<span data-ttu-id="122c5-123">Megadja azt az útvonalszűrőt, amelyhez ez a parancsmag hozzáad egy útvonalszűrő szabályt.</span><span class="sxs-lookup"><span data-stu-id="122c5-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="122c5-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="122c5-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="122c5-125">Az útvonalszűrő-szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="122c5-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="122c5-126">Érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="122c5-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="122c5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="122c5-127">-Confirm</span></span>
<span data-ttu-id="122c5-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="122c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="122c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122c5-129">-WhatIf</span></span>
<span data-ttu-id="122c5-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="122c5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="122c5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="122c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="122c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122c5-132">CommonParameters</span></span>
<span data-ttu-id="122c5-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122c5-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122c5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122c5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="122c5-135">INPUTS</span></span>

### <span data-ttu-id="122c5-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="122c5-136">PSRouteFilter</span></span>
<span data-ttu-id="122c5-137">A "RouteFilter" paraméter a "PSRouteFilter" típusú értéket fogadja el a folyamatból.</span><span class="sxs-lookup"><span data-stu-id="122c5-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="122c5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="122c5-138">OUTPUTS</span></span>

### <span data-ttu-id="122c5-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="122c5-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="122c5-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="122c5-140">NOTES</span></span>
<span data-ttu-id="122c5-141">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="122c5-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="122c5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="122c5-142">RELATED LINKS</span></span>

[<span data-ttu-id="122c5-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="122c5-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="122c5-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="122c5-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)




[<span data-ttu-id="122c5-145">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="122c5-145">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

