---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938530"
---
# <span data-ttu-id="48a1c-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="48a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="48a1c-103">Frissíti az útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="48a1c-103">Updates a route filter.</span></span>

## <span data-ttu-id="48a1c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48a1c-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48a1c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="48a1c-106">A **Set-AzApplicationGateway** parancsmag frissíti az útvonalszűrőt</span><span class="sxs-lookup"><span data-stu-id="48a1c-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="48a1c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="48a1c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="48a1c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="48a1c-109">Ez a parancs frissíti az útvonalszűrőt a $rf beállításával.</span><span class="sxs-lookup"><span data-stu-id="48a1c-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="48a1c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="48a1c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48a1c-111">-AsJob</span></span>
<span data-ttu-id="48a1c-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48a1c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="48a1c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48a1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48a1c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="48a1c-115">-Force</span></span>
<span data-ttu-id="48a1c-116">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="48a1c-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="48a1c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-117">-RouteFilter</span></span>
<span data-ttu-id="48a1c-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-118">The RouteFilter</span></span>

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

### <span data-ttu-id="48a1c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48a1c-119">-Confirm</span></span>
<span data-ttu-id="48a1c-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="48a1c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a1c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a1c-121">-WhatIf</span></span>
<span data-ttu-id="48a1c-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="48a1c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48a1c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48a1c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48a1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a1c-124">CommonParameters</span></span>
<span data-ttu-id="48a1c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a1c-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48a1c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a1c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48a1c-127">INPUTS</span></span>

### <span data-ttu-id="48a1c-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="48a1c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48a1c-129">OUTPUTS</span></span>

### <span data-ttu-id="48a1c-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="48a1c-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48a1c-131">NOTES</span></span>

## <span data-ttu-id="48a1c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48a1c-132">RELATED LINKS</span></span>

[<span data-ttu-id="48a1c-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="48a1c-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="48a1c-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="48a1c-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="48a1c-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48a1c-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="48a1c-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48a1c-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="48a1c-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48a1c-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="48a1c-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48a1c-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="48a1c-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48a1c-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
