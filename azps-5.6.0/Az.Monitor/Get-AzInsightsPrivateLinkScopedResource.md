---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932634"
---
# <span data-ttu-id="2cfca-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2cfca-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="2cfca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cfca-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfca-103">Get for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="2cfca-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="2cfca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cfca-104">SYNTAX</span></span>

### <span data-ttu-id="2cfca-105">ByScopeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2cfca-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cfca-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfca-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cfca-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfca-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cfca-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cfca-108">DESCRIPTION</span></span>
<span data-ttu-id="2cfca-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span><span class="sxs-lookup"><span data-stu-id="2cfca-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="2cfca-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cfca-110">EXAMPLES</span></span>

### <span data-ttu-id="2cfca-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2cfca-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="2cfca-112">List scoped resource under private link scope "scope_name"</span><span class="sxs-lookup"><span data-stu-id="2cfca-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="2cfca-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2cfca-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="2cfca-114">Hatókörű erőforrás lekérte "scope_name" nevű privát hivatkozás scoped_resource_name.</span><span class="sxs-lookup"><span data-stu-id="2cfca-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="2cfca-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cfca-115">PARAMETERS</span></span>

### <span data-ttu-id="2cfca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfca-116">-DefaultProfile</span></span>
<span data-ttu-id="2cfca-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cfca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cfca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cfca-118">-InputObject</span></span>
<span data-ttu-id="2cfca-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2cfca-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="2cfca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2cfca-120">-Name</span></span>
<span data-ttu-id="2cfca-121">Hatókörű erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="2cfca-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="2cfca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfca-122">-ResourceGroupName</span></span>
<span data-ttu-id="2cfca-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2cfca-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2cfca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cfca-124">-ResourceId</span></span>
<span data-ttu-id="2cfca-125">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2cfca-125">Resource Id</span></span>

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

### <span data-ttu-id="2cfca-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="2cfca-126">-ScopeName</span></span>
<span data-ttu-id="2cfca-127">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="2cfca-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="2cfca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfca-128">CommonParameters</span></span>
<span data-ttu-id="2cfca-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfca-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cfca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfca-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cfca-131">INPUTS</span></span>

### <span data-ttu-id="2cfca-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2cfca-132">System.String</span></span>

## <span data-ttu-id="2cfca-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cfca-133">OUTPUTS</span></span>

### <span data-ttu-id="2cfca-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2cfca-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="2cfca-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cfca-135">NOTES</span></span>

## <span data-ttu-id="2cfca-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cfca-136">RELATED LINKS</span></span>
