---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 5ae145c79012a62ae5e46c14bd649b17460f8d3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919658"
---
# <span data-ttu-id="c5cb0-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5cb0-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="c5cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5cb0-103">Útvonalszűrőt kap.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-103">Gets a route filter.</span></span>

## <span data-ttu-id="c5cb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5cb0-104">SYNTAX</span></span>

### <span data-ttu-id="c5cb0-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="c5cb0-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5cb0-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="c5cb0-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5cb0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="c5cb0-108">A **Get-AzRouteFilter** parancsmag útvonalszűrőt kap.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="c5cb0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5cb0-109">EXAMPLES</span></span>

### <span data-ttu-id="c5cb0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5cb0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="c5cb0-111">Ez a parancs a RouteFilter01 nevű útvonalszűrőt kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="c5cb0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c5cb0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="c5cb0-113">Ez a parancs az összes útvonalszűrőt beveszi, amelyek az "RouteFilter" kezdetekkel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="c5cb0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5cb0-114">PARAMETERS</span></span>

### <span data-ttu-id="c5cb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5cb0-115">-DefaultProfile</span></span>
<span data-ttu-id="c5cb0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5cb0-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c5cb0-117">-ExpandResource</span></span>
<span data-ttu-id="c5cb0-118">A kibontani szükséges erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5cb0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5cb0-119">-Name</span></span>
<span data-ttu-id="c5cb0-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c5cb0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5cb0-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5cb0-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c5cb0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5cb0-123">CommonParameters</span></span>
<span data-ttu-id="c5cb0-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5cb0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5cb0-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5cb0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5cb0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5cb0-126">INPUTS</span></span>

### <span data-ttu-id="c5cb0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c5cb0-127">System.String</span></span>

## <span data-ttu-id="c5cb0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5cb0-128">OUTPUTS</span></span>

### <span data-ttu-id="c5cb0-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5cb0-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c5cb0-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5cb0-130">NOTES</span></span>

## <span data-ttu-id="c5cb0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5cb0-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5cb0-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5cb0-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="c5cb0-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5cb0-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="c5cb0-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5cb0-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="c5cb0-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5cb0-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c5cb0-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5cb0-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c5cb0-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5cb0-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c5cb0-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5cb0-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c5cb0-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5cb0-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
