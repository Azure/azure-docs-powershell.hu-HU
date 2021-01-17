---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467272"
---
# <span data-ttu-id="a14dd-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="a14dd-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="a14dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a14dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a14dd-103">Irányítópult létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="a14dd-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a14dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a14dd-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a14dd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a14dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a14dd-106">Irányítópult létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="a14dd-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a14dd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a14dd-107">EXAMPLES</span></span>

### <span data-ttu-id="a14dd-108">1. példa: Az irányítópult definíciójának frissítése irányítópultsablon használatával</span><span class="sxs-lookup"><span data-stu-id="a14dd-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="a14dd-109">Irányítópult-definíció frissítése szaggatott vonalas sablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="a14dd-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="a14dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a14dd-110">PARAMETERS</span></span>

### <span data-ttu-id="a14dd-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="a14dd-111">-DashboardPath</span></span>
<span data-ttu-id="a14dd-112">The Path to an existing dashboard template.</span><span class="sxs-lookup"><span data-stu-id="a14dd-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="a14dd-113">Az irányítópultsablonok letölthetők a portálról.</span><span class="sxs-lookup"><span data-stu-id="a14dd-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="a14dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14dd-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a14dd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a14dd-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a14dd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14dd-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="a14dd-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a14dd-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a14dd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a14dd-118">-Confirm</span></span>
<span data-ttu-id="a14dd-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a14dd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a14dd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a14dd-120">-WhatIf</span></span>
<span data-ttu-id="a14dd-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a14dd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a14dd-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a14dd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a14dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14dd-123">CommonParameters</span></span>
<span data-ttu-id="a14dd-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14dd-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a14dd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14dd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a14dd-126">INPUTS</span></span>

## <span data-ttu-id="a14dd-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a14dd-127">OUTPUTS</span></span>

### <span data-ttu-id="a14dd-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="a14dd-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a14dd-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a14dd-129">NOTES</span></span>

<span data-ttu-id="a14dd-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a14dd-130">ALIASES</span></span>

## <span data-ttu-id="a14dd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a14dd-131">RELATED LINKS</span></span>

