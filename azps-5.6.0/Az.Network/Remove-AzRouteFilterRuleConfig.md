---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 2212ffb43f646e49a4552713b6408091dd985aae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941506"
---
# <span data-ttu-id="ebfa4-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebfa4-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ebfa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebfa4-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfa4-103">Eltávolít egy útvonalszűrő szabályt egy útvonalszűrőből.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="ebfa4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebfa4-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfa4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebfa4-105">DESCRIPTION</span></span>
<span data-ttu-id="ebfa4-106">A **Remove-AzRouteFilterRuleConfig** parancsmag eltávolít egy útvonalszűrő szabályt az útvonalszűrőkből.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="ebfa4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebfa4-107">EXAMPLES</span></span>

### <span data-ttu-id="ebfa4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ebfa4-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="ebfa4-109">Az első parancs egy RouteFilter01 nevű útvonalszűrőt kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és egy másik $rf tárolja.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="ebfa4-110">A második parancs eltávolítja a Szabály01 nevű útvonalszűrő-szabályt a $rf.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="ebfa4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebfa4-111">PARAMETERS</span></span>

### <span data-ttu-id="ebfa4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfa4-112">-DefaultProfile</span></span>
<span data-ttu-id="ebfa4-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebfa4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ebfa4-114">-Force</span></span>
<span data-ttu-id="ebfa4-115">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="ebfa4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ebfa4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ebfa4-116">-Name</span></span>
<span data-ttu-id="ebfa4-117">Az útvonalszűrő-szabály neve</span><span class="sxs-lookup"><span data-stu-id="ebfa4-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="ebfa4-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-118">-RouteFilter</span></span>
<span data-ttu-id="ebfa4-119">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-119">The RouteFilter</span></span>

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

### <span data-ttu-id="ebfa4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebfa4-120">-Confirm</span></span>
<span data-ttu-id="ebfa4-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebfa4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfa4-122">-WhatIf</span></span>
<span data-ttu-id="ebfa4-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebfa4-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebfa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfa4-125">CommonParameters</span></span>
<span data-ttu-id="ebfa4-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfa4-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfa4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfa4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebfa4-128">INPUTS</span></span>

### <span data-ttu-id="ebfa4-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ebfa4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebfa4-130">OUTPUTS</span></span>

### <span data-ttu-id="ebfa4-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ebfa4-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ebfa4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebfa4-132">NOTES</span></span>

## <span data-ttu-id="ebfa4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebfa4-133">RELATED LINKS</span></span>

[<span data-ttu-id="ebfa4-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebfa4-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebfa4-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebfa4-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebfa4-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebfa4-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebfa4-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebfa4-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebfa4-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ebfa4-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ebfa4-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ebfa4-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebfa4-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
