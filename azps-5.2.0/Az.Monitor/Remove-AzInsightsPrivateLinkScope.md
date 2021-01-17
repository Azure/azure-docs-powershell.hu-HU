---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345498"
---
# <span data-ttu-id="0c3df-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0c3df-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0c3df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3df-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3df-103">személyes hivatkozás hatókörének törlése</span><span class="sxs-lookup"><span data-stu-id="0c3df-103">delete private link scope</span></span>

## <span data-ttu-id="0c3df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c3df-104">SYNTAX</span></span>

### <span data-ttu-id="0c3df-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c3df-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3df-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3df-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3df-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3df-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3df-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c3df-108">DESCRIPTION</span></span>
<span data-ttu-id="0c3df-109">személyes hivatkozás hatókörének törlése</span><span class="sxs-lookup"><span data-stu-id="0c3df-109">delete private link scope</span></span>

## <span data-ttu-id="0c3df-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c3df-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3df-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0c3df-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="0c3df-112">Delete private link scope with name "scope_name" under resource group "rg_name"</span><span class="sxs-lookup"><span data-stu-id="0c3df-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="0c3df-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0c3df-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="0c3df-114">delete private link scope with resource Id</span><span class="sxs-lookup"><span data-stu-id="0c3df-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="0c3df-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="0c3df-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="0c3df-116">Delete private link scope with input private link scope object</span><span class="sxs-lookup"><span data-stu-id="0c3df-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="0c3df-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c3df-117">PARAMETERS</span></span>

### <span data-ttu-id="0c3df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3df-118">-DefaultProfile</span></span>
<span data-ttu-id="0c3df-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c3df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c3df-120">-InputObject</span></span>
<span data-ttu-id="0c3df-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0c3df-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="0c3df-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0c3df-122">-Name</span></span>
<span data-ttu-id="0c3df-123">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="0c3df-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="0c3df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3df-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c3df-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0c3df-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0c3df-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c3df-126">-ResourceId</span></span>
<span data-ttu-id="0c3df-127">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0c3df-127">Resource Id</span></span>

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

### <span data-ttu-id="0c3df-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c3df-128">-Confirm</span></span>
<span data-ttu-id="0c3df-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0c3df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3df-130">-WhatIf</span></span>
<span data-ttu-id="0c3df-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0c3df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3df-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c3df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3df-133">CommonParameters</span></span>
<span data-ttu-id="0c3df-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3df-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c3df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3df-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c3df-136">INPUTS</span></span>

### <span data-ttu-id="0c3df-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0c3df-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="0c3df-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0c3df-138">System.String</span></span>

## <span data-ttu-id="0c3df-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c3df-139">OUTPUTS</span></span>

### <span data-ttu-id="0c3df-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c3df-140">System.Boolean</span></span>

## <span data-ttu-id="0c3df-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c3df-141">NOTES</span></span>

## <span data-ttu-id="0c3df-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c3df-142">RELATED LINKS</span></span>
