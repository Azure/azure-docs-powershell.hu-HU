---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323326"
---
# <span data-ttu-id="4db00-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4db00-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4db00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db00-102">SYNOPSIS</span></span>
<span data-ttu-id="4db00-103">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="4db00-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="4db00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4db00-104">SYNTAX</span></span>

### <span data-ttu-id="4db00-105">ByScopeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4db00-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db00-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db00-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db00-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db00-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db00-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4db00-108">DESCRIPTION</span></span>
<span data-ttu-id="4db00-109">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="4db00-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="4db00-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4db00-110">EXAMPLES</span></span>

### <span data-ttu-id="4db00-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4db00-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="4db00-112">delete private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="4db00-112">delete private link scoped resource</span></span>

## <span data-ttu-id="4db00-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4db00-113">PARAMETERS</span></span>

### <span data-ttu-id="4db00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db00-114">-DefaultProfile</span></span>
<span data-ttu-id="4db00-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4db00-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db00-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4db00-116">-InputObject</span></span>
<span data-ttu-id="4db00-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4db00-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="4db00-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4db00-118">-Name</span></span>
<span data-ttu-id="4db00-119">Hatókörű erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4db00-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db00-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db00-120">-ResourceGroupName</span></span>
<span data-ttu-id="4db00-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4db00-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db00-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4db00-122">-ResourceId</span></span>
<span data-ttu-id="4db00-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4db00-123">Resource Id</span></span>

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

### <span data-ttu-id="4db00-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="4db00-124">-ScopeName</span></span>
<span data-ttu-id="4db00-125">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="4db00-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db00-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4db00-126">-Confirm</span></span>
<span data-ttu-id="4db00-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4db00-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db00-128">-WhatIf</span></span>
<span data-ttu-id="4db00-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4db00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db00-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4db00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db00-131">CommonParameters</span></span>
<span data-ttu-id="4db00-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db00-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4db00-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db00-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4db00-134">INPUTS</span></span>

### <span data-ttu-id="4db00-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4db00-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="4db00-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4db00-136">System.String</span></span>

## <span data-ttu-id="4db00-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4db00-137">OUTPUTS</span></span>

### <span data-ttu-id="4db00-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4db00-138">System.Boolean</span></span>

## <span data-ttu-id="4db00-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4db00-139">NOTES</span></span>

## <span data-ttu-id="4db00-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4db00-140">RELATED LINKS</span></span>
