---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 10ae3aab71cd977d3447501d13870eb10a8129ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009509"
---
# <span data-ttu-id="f2728-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f2728-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f2728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2728-102">SYNOPSIS</span></span>
<span data-ttu-id="f2728-103">create for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="f2728-103">create for private link scoped resource</span></span>

## <span data-ttu-id="f2728-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2728-104">SYNTAX</span></span>

### <span data-ttu-id="f2728-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2728-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2728-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2728-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2728-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2728-107">DESCRIPTION</span></span>
<span data-ttu-id="f2728-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span><span class="sxs-lookup"><span data-stu-id="f2728-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="f2728-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2728-109">EXAMPLES</span></span>

### <span data-ttu-id="f2728-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f2728-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="f2728-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span><span class="sxs-lookup"><span data-stu-id="f2728-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="f2728-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2728-112">PARAMETERS</span></span>

### <span data-ttu-id="f2728-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2728-113">-DefaultProfile</span></span>
<span data-ttu-id="f2728-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2728-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2728-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2728-115">-InputObject</span></span>
<span data-ttu-id="f2728-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f2728-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="f2728-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="f2728-117">-LinkedResourceId</span></span>
<span data-ttu-id="f2728-118">LA/AI Resource Id to Link</span><span class="sxs-lookup"><span data-stu-id="f2728-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="f2728-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f2728-119">-Name</span></span>
<span data-ttu-id="f2728-120">Hatókörű erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f2728-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="f2728-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2728-121">-ResourceGroupName</span></span>
<span data-ttu-id="f2728-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f2728-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f2728-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="f2728-123">-ScopeName</span></span>
<span data-ttu-id="f2728-124">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="f2728-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="f2728-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2728-125">-Confirm</span></span>
<span data-ttu-id="f2728-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f2728-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2728-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2728-127">-WhatIf</span></span>
<span data-ttu-id="f2728-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f2728-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2728-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2728-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2728-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2728-130">CommonParameters</span></span>
<span data-ttu-id="f2728-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2728-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2728-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2728-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2728-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2728-133">INPUTS</span></span>

### <span data-ttu-id="f2728-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f2728-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="f2728-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f2728-135">System.String</span></span>

## <span data-ttu-id="f2728-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2728-136">OUTPUTS</span></span>

### <span data-ttu-id="f2728-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f2728-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f2728-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2728-138">NOTES</span></span>

## <span data-ttu-id="f2728-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2728-139">RELATED LINKS</span></span>
