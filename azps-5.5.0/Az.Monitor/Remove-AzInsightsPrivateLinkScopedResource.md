---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147339"
---
# <span data-ttu-id="8646f-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="8646f-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="8646f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8646f-102">SYNOPSIS</span></span>
<span data-ttu-id="8646f-103">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="8646f-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="8646f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8646f-104">SYNTAX</span></span>

### <span data-ttu-id="8646f-105">ByScopeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8646f-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8646f-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8646f-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8646f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8646f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8646f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8646f-108">DESCRIPTION</span></span>
<span data-ttu-id="8646f-109">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="8646f-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="8646f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8646f-110">EXAMPLES</span></span>

### <span data-ttu-id="8646f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8646f-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="8646f-112">delete private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="8646f-112">delete private link scoped resource</span></span>

## <span data-ttu-id="8646f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8646f-113">PARAMETERS</span></span>

### <span data-ttu-id="8646f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8646f-114">-DefaultProfile</span></span>
<span data-ttu-id="8646f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8646f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8646f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8646f-116">-InputObject</span></span>
<span data-ttu-id="8646f-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="8646f-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="8646f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8646f-118">-Name</span></span>
<span data-ttu-id="8646f-119">Hatókörű erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="8646f-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="8646f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8646f-120">-ResourceGroupName</span></span>
<span data-ttu-id="8646f-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8646f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="8646f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8646f-122">-ResourceId</span></span>
<span data-ttu-id="8646f-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8646f-123">Resource Id</span></span>

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

### <span data-ttu-id="8646f-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="8646f-124">-ScopeName</span></span>
<span data-ttu-id="8646f-125">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="8646f-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="8646f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8646f-126">-Confirm</span></span>
<span data-ttu-id="8646f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8646f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8646f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8646f-128">-WhatIf</span></span>
<span data-ttu-id="8646f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8646f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8646f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8646f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8646f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8646f-131">CommonParameters</span></span>
<span data-ttu-id="8646f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8646f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8646f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8646f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8646f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8646f-134">INPUTS</span></span>

### <span data-ttu-id="8646f-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="8646f-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="8646f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8646f-136">System.String</span></span>

## <span data-ttu-id="8646f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8646f-137">OUTPUTS</span></span>

### <span data-ttu-id="8646f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8646f-138">System.Boolean</span></span>

## <span data-ttu-id="8646f-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8646f-139">NOTES</span></span>

## <span data-ttu-id="8646f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8646f-140">RELATED LINKS</span></span>
