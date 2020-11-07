---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 5222f6428bd7e57b71268465d60790869b12ef64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669973"
---
# <span data-ttu-id="59d92-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="59d92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59d92-102">SYNOPSIS</span></span>
<span data-ttu-id="59d92-103">Az útvonal-szűrő frissítése</span><span class="sxs-lookup"><span data-stu-id="59d92-103">Updates a route filter.</span></span>

## <span data-ttu-id="59d92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59d92-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59d92-105">DESCRIPTION</span></span>
<span data-ttu-id="59d92-106">A **set-AzApplicationGateway** parancsmag frissíti az útvonal-szűrőt</span><span class="sxs-lookup"><span data-stu-id="59d92-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="59d92-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59d92-107">EXAMPLES</span></span>

### <span data-ttu-id="59d92-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59d92-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="59d92-109">A parancs frissíti az útvonal-szűrőt a $rf változó beállításaival.</span><span class="sxs-lookup"><span data-stu-id="59d92-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="59d92-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59d92-110">PARAMETERS</span></span>

### <span data-ttu-id="59d92-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59d92-111">-AsJob</span></span>
<span data-ttu-id="59d92-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="59d92-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59d92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d92-113">-DefaultProfile</span></span>
<span data-ttu-id="59d92-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59d92-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d92-115">-Force</span><span class="sxs-lookup"><span data-stu-id="59d92-115">-Force</span></span>
<span data-ttu-id="59d92-116">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="59d92-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="59d92-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-117">-RouteFilter</span></span>
<span data-ttu-id="59d92-118">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-118">The RouteFilter</span></span>

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

### <span data-ttu-id="59d92-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59d92-119">-Confirm</span></span>
<span data-ttu-id="59d92-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59d92-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d92-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d92-121">-WhatIf</span></span>
<span data-ttu-id="59d92-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59d92-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59d92-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59d92-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d92-124">CommonParameters</span></span>
<span data-ttu-id="59d92-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59d92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d92-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d92-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d92-127">INPUTS</span></span>

### <span data-ttu-id="59d92-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="59d92-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d92-129">OUTPUTS</span></span>

### <span data-ttu-id="59d92-130">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="59d92-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59d92-131">NOTES</span></span>

## <span data-ttu-id="59d92-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59d92-132">RELATED LINKS</span></span>

[<span data-ttu-id="59d92-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="59d92-134">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="59d92-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59d92-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="59d92-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59d92-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59d92-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59d92-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59d92-138">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59d92-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59d92-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59d92-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59d92-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59d92-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
