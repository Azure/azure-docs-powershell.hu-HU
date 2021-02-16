---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151907"
---
# <span data-ttu-id="76f8c-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76f8c-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="76f8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="76f8c-103">Útvonalszűrő szabályt kap egy útvonalszűrőben.</span><span class="sxs-lookup"><span data-stu-id="76f8c-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="76f8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="76f8c-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76f8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="76f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="76f8c-106">A **Get-AzRouteFilterRuleConfig** parancsmag útvonalszűrő szabályt vagy útvonalszűrő szabályok listáját kapja meg egy útvonalszűrőben.</span><span class="sxs-lookup"><span data-stu-id="76f8c-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="76f8c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="76f8c-107">EXAMPLES</span></span>

### <span data-ttu-id="76f8c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="76f8c-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="76f8c-109">Az első parancs leküldi a MyRouteFilter nevű útvonalszűrőt, majd tárolja azt a $rf.</span><span class="sxs-lookup"><span data-stu-id="76f8c-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="76f8c-110">A második parancs az adott útvonalszűrővel társított Szabály01 nevű útvonalszűrő-szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="76f8c-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="76f8c-111">A harmadik parancs az adott útvonalszűrővel társított útvonalszűrő-szabályok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="76f8c-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="76f8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f8c-112">PARAMETERS</span></span>

### <span data-ttu-id="76f8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f8c-113">-DefaultProfile</span></span>
<span data-ttu-id="76f8c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76f8c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76f8c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="76f8c-115">-Name</span></span>
<span data-ttu-id="76f8c-116">Az útvonalszűrő-szabály neve</span><span class="sxs-lookup"><span data-stu-id="76f8c-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f8c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-117">-RouteFilter</span></span>
<span data-ttu-id="76f8c-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-118">The RouteFilter</span></span>

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

### <span data-ttu-id="76f8c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f8c-119">CommonParameters</span></span>
<span data-ttu-id="76f8c-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f8c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f8c-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76f8c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f8c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76f8c-122">INPUTS</span></span>

### <span data-ttu-id="76f8c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="76f8c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76f8c-124">OUTPUTS</span></span>

### <span data-ttu-id="76f8c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="76f8c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="76f8c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="76f8c-126">NOTES</span></span>

## <span data-ttu-id="76f8c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76f8c-127">RELATED LINKS</span></span>

[<span data-ttu-id="76f8c-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76f8c-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76f8c-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76f8c-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76f8c-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76f8c-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76f8c-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76f8c-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76f8c-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="76f8c-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="76f8c-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="76f8c-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76f8c-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
