---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470097"
---
# <span data-ttu-id="40db0-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="40db0-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="40db0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40db0-102">SYNOPSIS</span></span>
<span data-ttu-id="40db0-103">Irányítópult létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="40db0-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="40db0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40db0-104">SYNTAX</span></span>

### <span data-ttu-id="40db0-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40db0-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40db0-106">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="40db0-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40db0-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="40db0-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40db0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40db0-108">DESCRIPTION</span></span>
<span data-ttu-id="40db0-109">Irányítópult létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="40db0-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="40db0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40db0-110">EXAMPLES</span></span>

### <span data-ttu-id="40db0-111">1. példa: Irányítópult létrehozása irányítópultsablonfájl használatával</span><span class="sxs-lookup"><span data-stu-id="40db0-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="40db0-112">Hozzon létre egy új irányítópultot a megadott irányítópultsablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="40db0-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="40db0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40db0-113">PARAMETERS</span></span>

### <span data-ttu-id="40db0-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="40db0-114">-Dashboard</span></span>
<span data-ttu-id="40db0-115">A megosztott irányítópult erőforrás-definíciója.</span><span class="sxs-lookup"><span data-stu-id="40db0-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="40db0-116">Ennek létrehozásáról az IRÁNYÍTÓPULT tulajdonságairól és a kivonattáblák létrehozásáról a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="40db0-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40db0-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="40db0-117">-DashboardPath</span></span>
<span data-ttu-id="40db0-118">The Path to an existing dashboard template.</span><span class="sxs-lookup"><span data-stu-id="40db0-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="40db0-119">Az irányítópultsablonok letölthetők a portálról.</span><span class="sxs-lookup"><span data-stu-id="40db0-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40db0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40db0-120">-DefaultProfile</span></span>
<span data-ttu-id="40db0-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40db0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40db0-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="40db0-122">-Lens</span></span>
<span data-ttu-id="40db0-123">Az irányítópult lenjei.</span><span class="sxs-lookup"><span data-stu-id="40db0-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40db0-124">-Location</span><span class="sxs-lookup"><span data-stu-id="40db0-124">-Location</span></span>
<span data-ttu-id="40db0-125">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="40db0-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40db0-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="40db0-126">-Metadata</span></span>
<span data-ttu-id="40db0-127">Az irányítópult metaadatai.</span><span class="sxs-lookup"><span data-stu-id="40db0-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40db0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="40db0-128">-Name</span></span>
<span data-ttu-id="40db0-129">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="40db0-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="40db0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40db0-130">-ResourceGroupName</span></span>
<span data-ttu-id="40db0-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40db0-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="40db0-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40db0-132">-SubscriptionId</span></span>
<span data-ttu-id="40db0-133">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="40db0-133">The Azure subscription ID.</span></span>
<span data-ttu-id="40db0-134">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="40db0-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="40db0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="40db0-135">-Tag</span></span>
<span data-ttu-id="40db0-136">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="40db0-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40db0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40db0-137">-Confirm</span></span>
<span data-ttu-id="40db0-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40db0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40db0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40db0-139">-WhatIf</span></span>
<span data-ttu-id="40db0-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40db0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40db0-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40db0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40db0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40db0-142">CommonParameters</span></span>
<span data-ttu-id="40db0-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40db0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40db0-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40db0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40db0-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40db0-145">INPUTS</span></span>

### <span data-ttu-id="40db0-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="40db0-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="40db0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40db0-147">OUTPUTS</span></span>

### <span data-ttu-id="40db0-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="40db0-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="40db0-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40db0-149">NOTES</span></span>

<span data-ttu-id="40db0-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="40db0-150">ALIASES</span></span>

<span data-ttu-id="40db0-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="40db0-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40db0-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="40db0-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40db0-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40db0-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40db0-154">IRÁNYÍTÓPULT: <IDashboard> A megosztott irányítópult erőforrás-definíciója.</span><span class="sxs-lookup"><span data-stu-id="40db0-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="40db0-155">`Location <String>`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="40db0-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="40db0-156">`[Lens <IDashboardPropertiesLenses>]`: Az irányítópult lenjei.</span><span class="sxs-lookup"><span data-stu-id="40db0-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="40db0-157">`[(Any) <IDashboardLens>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="40db0-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="40db0-158">`[Metadata <IDashboardPropertiesMetadata>]`: Az irányítópult metaadatai.</span><span class="sxs-lookup"><span data-stu-id="40db0-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="40db0-159">`[(Any) <Object>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="40db0-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="40db0-160">`[Tag <IDashboardTags>]`: Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="40db0-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="40db0-161">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="40db0-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="40db0-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40db0-162">RELATED LINKS</span></span>

