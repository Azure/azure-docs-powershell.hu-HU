---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: dbd1564ceb4a4315f62f11712c73c56b46dcff7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921714"
---
# <span data-ttu-id="6de86-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6de86-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="6de86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de86-102">SYNOPSIS</span></span>
<span data-ttu-id="6de86-103">Útvonalszűrő szabályt hoz létre az útvonalszűrők számára.</span><span class="sxs-lookup"><span data-stu-id="6de86-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="6de86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6de86-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de86-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6de86-105">DESCRIPTION</span></span>
<span data-ttu-id="6de86-106">A New-AzRouteFilterRuleConfig parancsmag létrehoz egy útvonalszűrő szabályt egy Azure-útvonalszűrő számára.</span><span class="sxs-lookup"><span data-stu-id="6de86-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="6de86-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6de86-107">EXAMPLES</span></span>

### <span data-ttu-id="6de86-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6de86-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="6de86-109">A parancs létrehoz egy új útvonalszűrő szabályt, és azt egy változó $rule 1.</span><span class="sxs-lookup"><span data-stu-id="6de86-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="6de86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6de86-110">PARAMETERS</span></span>

### <span data-ttu-id="6de86-111">-Access</span><span class="sxs-lookup"><span data-stu-id="6de86-111">-Access</span></span>
<span data-ttu-id="6de86-112">Útvonalszűrő-szabály elérése</span><span class="sxs-lookup"><span data-stu-id="6de86-112">Access for route filter rule.</span></span>
<span data-ttu-id="6de86-113">Érvényes értékek: Allow vagy Deny.</span><span class="sxs-lookup"><span data-stu-id="6de86-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="6de86-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="6de86-114">-CommunityList</span></span>
<span data-ttu-id="6de86-115">Az útvonalszűrőt szűrő közösségi értékek listája</span><span class="sxs-lookup"><span data-stu-id="6de86-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="6de86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de86-116">-DefaultProfile</span></span>
<span data-ttu-id="6de86-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6de86-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de86-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6de86-118">-Force</span></span>
<span data-ttu-id="6de86-119">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="6de86-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6de86-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6de86-120">-Name</span></span>
<span data-ttu-id="6de86-121">Megadja az útvonalszűrő-szabály nevét.</span><span class="sxs-lookup"><span data-stu-id="6de86-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="6de86-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="6de86-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="6de86-123">Útvonalszűrő szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="6de86-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="6de86-124">Érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="6de86-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="6de86-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6de86-125">-Confirm</span></span>
<span data-ttu-id="6de86-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6de86-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de86-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de86-127">-WhatIf</span></span>
<span data-ttu-id="6de86-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6de86-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6de86-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6de86-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de86-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de86-130">CommonParameters</span></span>
<span data-ttu-id="6de86-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de86-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de86-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de86-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de86-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6de86-133">INPUTS</span></span>

### <span data-ttu-id="6de86-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="6de86-134">None</span></span>

## <span data-ttu-id="6de86-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6de86-135">OUTPUTS</span></span>

### <span data-ttu-id="6de86-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="6de86-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="6de86-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6de86-137">NOTES</span></span>
<span data-ttu-id="6de86-138">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="6de86-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6de86-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6de86-139">RELATED LINKS</span></span>

[<span data-ttu-id="6de86-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6de86-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6de86-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6de86-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6de86-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6de86-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6de86-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6de86-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6de86-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6de86-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6de86-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6de86-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="6de86-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6de86-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="6de86-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6de86-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
