---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207142"
---
# <span data-ttu-id="db23d-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="db23d-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="db23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db23d-102">SYNOPSIS</span></span>
<span data-ttu-id="db23d-103">Get for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="db23d-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="db23d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db23d-104">SYNTAX</span></span>

### <span data-ttu-id="db23d-105">ByScopeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db23d-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db23d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db23d-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db23d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db23d-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db23d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db23d-108">DESCRIPTION</span></span>
<span data-ttu-id="db23d-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span><span class="sxs-lookup"><span data-stu-id="db23d-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="db23d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db23d-110">EXAMPLES</span></span>

### <span data-ttu-id="db23d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="db23d-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="db23d-112">List scoped resource under private link scope "scope_name"</span><span class="sxs-lookup"><span data-stu-id="db23d-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="db23d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="db23d-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="db23d-114">Hatókörű erőforrás lekérte "scope_name" nevű privát hivatkozás scoped_resource_name.</span><span class="sxs-lookup"><span data-stu-id="db23d-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="db23d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db23d-115">PARAMETERS</span></span>

### <span data-ttu-id="db23d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db23d-116">-DefaultProfile</span></span>
<span data-ttu-id="db23d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db23d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db23d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db23d-118">-InputObject</span></span>
<span data-ttu-id="db23d-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="db23d-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db23d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="db23d-120">-Name</span></span>
<span data-ttu-id="db23d-121">Hatókörű erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="db23d-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db23d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db23d-122">-ResourceGroupName</span></span>
<span data-ttu-id="db23d-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="db23d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="db23d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db23d-124">-ResourceId</span></span>
<span data-ttu-id="db23d-125">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="db23d-125">Resource Id</span></span>

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

### <span data-ttu-id="db23d-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="db23d-126">-ScopeName</span></span>
<span data-ttu-id="db23d-127">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="db23d-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="db23d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db23d-128">CommonParameters</span></span>
<span data-ttu-id="db23d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db23d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db23d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db23d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db23d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db23d-131">INPUTS</span></span>

### <span data-ttu-id="db23d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="db23d-132">System.String</span></span>

## <span data-ttu-id="db23d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db23d-133">OUTPUTS</span></span>

### <span data-ttu-id="db23d-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="db23d-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="db23d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db23d-135">NOTES</span></span>

## <span data-ttu-id="db23d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db23d-136">RELATED LINKS</span></span>
