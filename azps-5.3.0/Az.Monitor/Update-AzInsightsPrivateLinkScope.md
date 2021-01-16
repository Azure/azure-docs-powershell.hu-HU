---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466302"
---
# <span data-ttu-id="4eb2a-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4eb2a-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="4eb2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb2a-103">Frissítés a magánjellegű hivatkozás hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="4eb2a-103">Update for private link scope</span></span>

## <span data-ttu-id="4eb2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4eb2a-104">SYNTAX</span></span>

### <span data-ttu-id="4eb2a-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4eb2a-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb2a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb2a-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb2a-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb2a-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb2a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4eb2a-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb2a-109">Frissítés a magánjellegű hivatkozás hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="4eb2a-109">Update for private link scope</span></span>

## <span data-ttu-id="4eb2a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4eb2a-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb2a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4eb2a-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="4eb2a-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="4eb2a-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="4eb2a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4eb2a-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="4eb2a-114">update private link scope with resource Id to use tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="4eb2a-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="4eb2a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="4eb2a-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="4eb2a-116">update private link scope with input private link scope object to use tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="4eb2a-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="4eb2a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb2a-117">PARAMETERS</span></span>

### <span data-ttu-id="4eb2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb2a-118">-DefaultProfile</span></span>
<span data-ttu-id="4eb2a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4eb2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb2a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb2a-120">-InputObject</span></span>
<span data-ttu-id="4eb2a-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4eb2a-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="4eb2a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb2a-122">-Name</span></span>
<span data-ttu-id="4eb2a-123">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="4eb2a-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="4eb2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4eb2a-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4eb2a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="4eb2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb2a-126">-ResourceId</span></span>
<span data-ttu-id="4eb2a-127">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4eb2a-127">Resource Id</span></span>

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

### <span data-ttu-id="4eb2a-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="4eb2a-128">-Tags</span></span>
<span data-ttu-id="4eb2a-129">Címkék</span><span class="sxs-lookup"><span data-stu-id="4eb2a-129">Tags</span></span>

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

### <span data-ttu-id="4eb2a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eb2a-130">-Confirm</span></span>
<span data-ttu-id="4eb2a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4eb2a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb2a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb2a-132">-WhatIf</span></span>
<span data-ttu-id="4eb2a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4eb2a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb2a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4eb2a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb2a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb2a-135">CommonParameters</span></span>
<span data-ttu-id="4eb2a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb2a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb2a-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eb2a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb2a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb2a-138">INPUTS</span></span>

### <span data-ttu-id="4eb2a-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4eb2a-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="4eb2a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb2a-140">System.String</span></span>

## <span data-ttu-id="4eb2a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eb2a-141">OUTPUTS</span></span>

### <span data-ttu-id="4eb2a-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4eb2a-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="4eb2a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4eb2a-143">NOTES</span></span>

## <span data-ttu-id="4eb2a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eb2a-144">RELATED LINKS</span></span>
