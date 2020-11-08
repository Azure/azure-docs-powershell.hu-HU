---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195402"
---
# <span data-ttu-id="06cac-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="06cac-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="06cac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06cac-102">SYNOPSIS</span></span>
<span data-ttu-id="06cac-103">Az útvonaltervezés szabályait az útvonal-szűrőben kapja.</span><span class="sxs-lookup"><span data-stu-id="06cac-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="06cac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06cac-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06cac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06cac-105">DESCRIPTION</span></span>
<span data-ttu-id="06cac-106">A **Get-AzRouteFilterRuleConfig** parancsmag az útvonaltervezés szabályait vagy az útvonal-szűrési szabályok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="06cac-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="06cac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06cac-107">EXAMPLES</span></span>

### <span data-ttu-id="06cac-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06cac-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="06cac-109">Az első parancs a MyRouteFilter nevű útvonal-szűrőt kapja meg, majd a változóban tárolja $rf.</span><span class="sxs-lookup"><span data-stu-id="06cac-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="06cac-110">A második parancs az Rule01 társított, az útválasztási szűrőhöz társított útvonal-szűrő szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="06cac-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="06cac-111">A harmadik parancs az adott útvonal-szűrőhöz társított útvonal-szűrési szabályok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="06cac-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="06cac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06cac-112">PARAMETERS</span></span>

### <span data-ttu-id="06cac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cac-113">-DefaultProfile</span></span>
<span data-ttu-id="06cac-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06cac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06cac-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06cac-115">-Name</span></span>
<span data-ttu-id="06cac-116">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="06cac-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="06cac-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-117">-RouteFilter</span></span>
<span data-ttu-id="06cac-118">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-118">The RouteFilter</span></span>

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

### <span data-ttu-id="06cac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cac-119">CommonParameters</span></span>
<span data-ttu-id="06cac-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06cac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06cac-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06cac-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cac-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06cac-122">INPUTS</span></span>

### <span data-ttu-id="06cac-123">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="06cac-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06cac-124">OUTPUTS</span></span>

### <span data-ttu-id="06cac-125">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="06cac-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="06cac-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06cac-126">NOTES</span></span>

## <span data-ttu-id="06cac-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06cac-127">RELATED LINKS</span></span>

[<span data-ttu-id="06cac-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="06cac-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="06cac-129">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="06cac-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="06cac-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="06cac-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="06cac-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="06cac-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="06cac-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="06cac-133">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="06cac-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="06cac-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="06cac-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
