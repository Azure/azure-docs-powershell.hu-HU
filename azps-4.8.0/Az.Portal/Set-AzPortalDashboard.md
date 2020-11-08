---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184291"
---
# <span data-ttu-id="9f9dc-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="9f9dc-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="9f9dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="9f9dc-103">Irányítópultot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="9f9dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f9dc-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f9dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="9f9dc-106">Irányítópultot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="9f9dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9f9dc-107">EXAMPLES</span></span>

### <span data-ttu-id="9f9dc-108">1. példa: az irányítópult-definíció frissítése irányítópult-sablon használatával</span><span class="sxs-lookup"><span data-stu-id="9f9dc-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="9f9dc-109">Irányítópult-definíció frissítése dashbaord-sablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="9f9dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f9dc-110">PARAMETERS</span></span>

### <span data-ttu-id="9f9dc-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="9f9dc-111">-DashboardPath</span></span>
<span data-ttu-id="9f9dc-112">A meglévő irányítópult-sablon elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="9f9dc-113">Lehet, hogy a portálról tölthetők le az irányítópult-sablonok.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="9f9dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f9dc-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="9f9dc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f9dc-115">-Name</span></span>


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

### <span data-ttu-id="9f9dc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f9dc-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="9f9dc-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f9dc-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="9f9dc-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f9dc-118">-Confirm</span></span>
<span data-ttu-id="9f9dc-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f9dc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f9dc-120">-WhatIf</span></span>
<span data-ttu-id="9f9dc-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f9dc-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f9dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f9dc-123">CommonParameters</span></span>
<span data-ttu-id="9f9dc-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f9dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f9dc-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f9dc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f9dc-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f9dc-126">INPUTS</span></span>

## <span data-ttu-id="9f9dc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f9dc-127">OUTPUTS</span></span>

### <span data-ttu-id="9f9dc-128">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="9f9dc-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="9f9dc-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f9dc-129">NOTES</span></span>

<span data-ttu-id="9f9dc-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9f9dc-130">ALIASES</span></span>

## <span data-ttu-id="9f9dc-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f9dc-131">RELATED LINKS</span></span>

