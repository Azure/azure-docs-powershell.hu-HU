---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301310"
---
# <span data-ttu-id="cd77f-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="cd77f-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="cd77f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd77f-102">SYNOPSIS</span></span>
<span data-ttu-id="cd77f-103">Irányítópultot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="cd77f-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="cd77f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd77f-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd77f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd77f-105">DESCRIPTION</span></span>
<span data-ttu-id="cd77f-106">Irányítópultot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="cd77f-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="cd77f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd77f-107">EXAMPLES</span></span>

### <span data-ttu-id="cd77f-108">1. példa: az irányítópult-definíció frissítése irányítópult-sablon használatával</span><span class="sxs-lookup"><span data-stu-id="cd77f-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="cd77f-109">Irányítópult-definíció frissítése dashbaord-sablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="cd77f-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="cd77f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd77f-110">PARAMETERS</span></span>

### <span data-ttu-id="cd77f-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="cd77f-111">-DashboardPath</span></span>
<span data-ttu-id="cd77f-112">A meglévő irányítópult-sablon elérési útja.</span><span class="sxs-lookup"><span data-stu-id="cd77f-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="cd77f-113">Lehet, hogy a portálról tölthetők le az irányítópult-sablonok.</span><span class="sxs-lookup"><span data-stu-id="cd77f-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="cd77f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd77f-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="cd77f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd77f-115">-Name</span></span>


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

### <span data-ttu-id="cd77f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd77f-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="cd77f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd77f-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="cd77f-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd77f-118">-Confirm</span></span>
<span data-ttu-id="cd77f-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd77f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd77f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd77f-120">-WhatIf</span></span>
<span data-ttu-id="cd77f-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd77f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd77f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd77f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd77f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd77f-123">CommonParameters</span></span>
<span data-ttu-id="cd77f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd77f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd77f-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd77f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd77f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd77f-126">INPUTS</span></span>

## <span data-ttu-id="cd77f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd77f-127">OUTPUTS</span></span>

### <span data-ttu-id="cd77f-128">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="cd77f-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="cd77f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd77f-129">NOTES</span></span>

<span data-ttu-id="cd77f-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cd77f-130">ALIASES</span></span>

## <span data-ttu-id="cd77f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd77f-131">RELATED LINKS</span></span>

