---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479896"
---
# <span data-ttu-id="7e590-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e590-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="7e590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e590-102">SYNOPSIS</span></span>
<span data-ttu-id="7e590-103">Módosítja egy útvonalszűrő útvonalszűrő-szabályát.</span><span class="sxs-lookup"><span data-stu-id="7e590-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="7e590-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e590-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e590-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e590-105">DESCRIPTION</span></span>
<span data-ttu-id="7e590-106">A **Set-AzRouteFilterRuleConfig** parancsmag módosítja egy útvonalszűrő útvonalszűrő szabályát.</span><span class="sxs-lookup"><span data-stu-id="7e590-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="7e590-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e590-107">EXAMPLES</span></span>

### <span data-ttu-id="7e590-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e590-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="7e590-109">Az első parancs megkapja a RouteFilter01 nevű útvonalszűrőt, és a szűrőt a $rf tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e590-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="7e590-110">A második parancs módosítja a Szabály01 nevű útvonalszűrő szabályt, és a frissített útvonalszűrőt tárolja a $rf változóban.</span><span class="sxs-lookup"><span data-stu-id="7e590-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="7e590-111">A harmadik parancs menti a frissített útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="7e590-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="7e590-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e590-112">PARAMETERS</span></span>

### <span data-ttu-id="7e590-113">-Access</span><span class="sxs-lookup"><span data-stu-id="7e590-113">-Access</span></span>
<span data-ttu-id="7e590-114">A szabály hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="7e590-114">The access type of the rule.</span></span>
<span data-ttu-id="7e590-115">Lehetséges értékek: "Megengedve", "Elutasítás"</span><span class="sxs-lookup"><span data-stu-id="7e590-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="7e590-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="7e590-116">-CommunityList</span></span>
<span data-ttu-id="7e590-117">Az útvonalszűrőt szűrő közösségi értékek listája</span><span class="sxs-lookup"><span data-stu-id="7e590-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="7e590-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e590-118">-DefaultProfile</span></span>
<span data-ttu-id="7e590-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e590-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e590-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e590-120">-Force</span></span>
<span data-ttu-id="7e590-121">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="7e590-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7e590-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7e590-122">-Name</span></span>
<span data-ttu-id="7e590-123">Az útvonalszűrő-szabály neve</span><span class="sxs-lookup"><span data-stu-id="7e590-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="7e590-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-124">-RouteFilter</span></span>
<span data-ttu-id="7e590-125">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-125">The RouteFilter</span></span>

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

### <span data-ttu-id="7e590-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="7e590-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="7e590-127">A szabály útvonalszűrő szabálytípusa.</span><span class="sxs-lookup"><span data-stu-id="7e590-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="7e590-128">Lehetséges értékek: "Közösség"</span><span class="sxs-lookup"><span data-stu-id="7e590-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="7e590-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e590-129">-Confirm</span></span>
<span data-ttu-id="7e590-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e590-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e590-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e590-131">-WhatIf</span></span>
<span data-ttu-id="7e590-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e590-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e590-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e590-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e590-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e590-134">CommonParameters</span></span>
<span data-ttu-id="7e590-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e590-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e590-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e590-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e590-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e590-137">INPUTS</span></span>

### <span data-ttu-id="7e590-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7e590-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e590-139">OUTPUTS</span></span>

### <span data-ttu-id="7e590-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7e590-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e590-141">NOTES</span></span>

## <span data-ttu-id="7e590-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e590-142">RELATED LINKS</span></span>

[<span data-ttu-id="7e590-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e590-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7e590-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e590-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7e590-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e590-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7e590-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e590-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7e590-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="7e590-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="7e590-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="7e590-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e590-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
