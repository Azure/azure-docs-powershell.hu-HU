---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ef53c93669faea2e9f952c0887e6cb0b105cf19b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925497"
---
# <span data-ttu-id="cd946-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd946-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="cd946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd946-102">SYNOPSIS</span></span>
<span data-ttu-id="cd946-103">Frissítés a magánjellegű hivatkozás hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="cd946-103">Update for private link scope</span></span>

## <span data-ttu-id="cd946-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd946-104">SYNTAX</span></span>

### <span data-ttu-id="cd946-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd946-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd946-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd946-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd946-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd946-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd946-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd946-108">DESCRIPTION</span></span>
<span data-ttu-id="cd946-109">Frissítés a magánjellegű hivatkozás hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="cd946-109">Update for private link scope</span></span>

## <span data-ttu-id="cd946-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd946-110">EXAMPLES</span></span>

### <span data-ttu-id="cd946-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cd946-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="cd946-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="cd946-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="cd946-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cd946-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="cd946-114">update private link scope with resource Id to use tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="cd946-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="cd946-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="cd946-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="cd946-116">update private link scope with input private link scope object to use tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="cd946-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="cd946-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd946-117">PARAMETERS</span></span>

### <span data-ttu-id="cd946-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd946-118">-DefaultProfile</span></span>
<span data-ttu-id="cd946-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd946-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd946-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd946-120">-InputObject</span></span>
<span data-ttu-id="cd946-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd946-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd946-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cd946-122">-Name</span></span>
<span data-ttu-id="cd946-123">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="cd946-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd946-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd946-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd946-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cd946-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd946-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd946-126">-ResourceId</span></span>
<span data-ttu-id="cd946-127">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cd946-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd946-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="cd946-128">-Tags</span></span>
<span data-ttu-id="cd946-129">Címkék</span><span class="sxs-lookup"><span data-stu-id="cd946-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd946-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd946-130">-Confirm</span></span>
<span data-ttu-id="cd946-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd946-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd946-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd946-132">-WhatIf</span></span>
<span data-ttu-id="cd946-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd946-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd946-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd946-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd946-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd946-135">CommonParameters</span></span>
<span data-ttu-id="cd946-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd946-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd946-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd946-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd946-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd946-138">INPUTS</span></span>

### <span data-ttu-id="cd946-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd946-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="cd946-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cd946-140">System.String</span></span>

## <span data-ttu-id="cd946-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd946-141">OUTPUTS</span></span>

### <span data-ttu-id="cd946-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd946-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="cd946-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd946-143">NOTES</span></span>

## <span data-ttu-id="cd946-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd946-144">RELATED LINKS</span></span>
