---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013294"
---
# <span data-ttu-id="7b2c8-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7b2c8-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="7b2c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2c8-103">Beolvassa az útvonal szűrőt.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-103">Gets a route filter.</span></span>

## <span data-ttu-id="7b2c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b2c8-104">SYNTAX</span></span>

### <span data-ttu-id="7b2c8-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="7b2c8-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b2c8-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="7b2c8-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2c8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b2c8-107">DESCRIPTION</span></span>
<span data-ttu-id="7b2c8-108">A **Get-AzRouteFilter** parancsmag átadja az útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="7b2c8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7b2c8-109">EXAMPLES</span></span>

### <span data-ttu-id="7b2c8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b2c8-110">Example 1</span></span>
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

<span data-ttu-id="7b2c8-111">Ez a parancs beolvassa a RouteFilter01 nevű útvonal-szűrőt, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="7b2c8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7b2c8-112">Example 2</span></span>
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

<span data-ttu-id="7b2c8-113">Ez a parancs a "RouteFilter" kezdetű összes útvonal-szűrőt megkapja.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="7b2c8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b2c8-114">PARAMETERS</span></span>

### <span data-ttu-id="7b2c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2c8-115">-DefaultProfile</span></span>
<span data-ttu-id="7b2c8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b2c8-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7b2c8-117">-ExpandResource</span></span>
<span data-ttu-id="7b2c8-118">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="7b2c8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b2c8-119">-Name</span></span>
<span data-ttu-id="7b2c8-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-120">The resource name.</span></span>

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

### <span data-ttu-id="7b2c8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2c8-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b2c8-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-122">The resource group name.</span></span>

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

### <span data-ttu-id="7b2c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2c8-123">CommonParameters</span></span>
<span data-ttu-id="7b2c8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b2c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2c8-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2c8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b2c8-126">INPUTS</span></span>

### <span data-ttu-id="7b2c8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7b2c8-127">System.String</span></span>

## <span data-ttu-id="7b2c8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b2c8-128">OUTPUTS</span></span>

### <span data-ttu-id="7b2c8-129">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7b2c8-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7b2c8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b2c8-130">NOTES</span></span>

## <span data-ttu-id="7b2c8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b2c8-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b2c8-132">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7b2c8-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="7b2c8-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7b2c8-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="7b2c8-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7b2c8-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="7b2c8-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b2c8-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7b2c8-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b2c8-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7b2c8-137">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b2c8-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7b2c8-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b2c8-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7b2c8-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b2c8-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
