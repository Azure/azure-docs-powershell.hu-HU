---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184280"
---
# <span data-ttu-id="db3b8-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="db3b8-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="db3b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="db3b8-103">Irányítópultot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="db3b8-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="db3b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db3b8-104">SYNTAX</span></span>

### <span data-ttu-id="db3b8-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db3b8-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db3b8-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="db3b8-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db3b8-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="db3b8-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db3b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="db3b8-108">DESCRIPTION</span></span>
<span data-ttu-id="db3b8-109">Irányítópultot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="db3b8-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="db3b8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="db3b8-110">EXAMPLES</span></span>

### <span data-ttu-id="db3b8-111">1. példa: irányítópult létrehozása irányítópult-sablonfájl használatával</span><span class="sxs-lookup"><span data-stu-id="db3b8-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="db3b8-112">Hozzon létre egy új irányítópultot a mellékelt irányítópult-sablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="db3b8-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="db3b8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db3b8-113">PARAMETERS</span></span>

### <span data-ttu-id="db3b8-114">-Irányítópult</span><span class="sxs-lookup"><span data-stu-id="db3b8-114">-Dashboard</span></span>
<span data-ttu-id="db3b8-115">A megosztott irányítópult erőforrás-definíciója.</span><span class="sxs-lookup"><span data-stu-id="db3b8-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="db3b8-116">A kivitelezéshez lásd: a jegyzetek szakasz az irányítópult tulajdonságaihoz, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="db3b8-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="db3b8-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="db3b8-117">-DashboardPath</span></span>
<span data-ttu-id="db3b8-118">A meglévő irányítópult-sablon elérési útja.</span><span class="sxs-lookup"><span data-stu-id="db3b8-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="db3b8-119">Lehet, hogy a portálról tölthetők le az irányítópult-sablonok.</span><span class="sxs-lookup"><span data-stu-id="db3b8-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="db3b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3b8-120">-DefaultProfile</span></span>
<span data-ttu-id="db3b8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db3b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db3b8-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="db3b8-122">-Lens</span></span>
<span data-ttu-id="db3b8-123">Az irányítópult lencséi.</span><span class="sxs-lookup"><span data-stu-id="db3b8-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="db3b8-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="db3b8-124">-Location</span></span>
<span data-ttu-id="db3b8-125">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="db3b8-125">Resource location</span></span>

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

### <span data-ttu-id="db3b8-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="db3b8-126">-Metadata</span></span>
<span data-ttu-id="db3b8-127">Az irányítópult metaadatai.</span><span class="sxs-lookup"><span data-stu-id="db3b8-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="db3b8-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db3b8-128">-Name</span></span>
<span data-ttu-id="db3b8-129">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="db3b8-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="db3b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="db3b8-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db3b8-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="db3b8-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db3b8-132">-SubscriptionId</span></span>
<span data-ttu-id="db3b8-133">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db3b8-133">The Azure subscription ID.</span></span>
<span data-ttu-id="db3b8-134">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="db3b8-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="db3b8-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="db3b8-135">-Tag</span></span>
<span data-ttu-id="db3b8-136">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="db3b8-136">Resource tags</span></span>

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

### <span data-ttu-id="db3b8-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db3b8-137">-Confirm</span></span>
<span data-ttu-id="db3b8-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db3b8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3b8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db3b8-139">-WhatIf</span></span>
<span data-ttu-id="db3b8-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db3b8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db3b8-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db3b8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3b8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3b8-142">CommonParameters</span></span>
<span data-ttu-id="db3b8-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db3b8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3b8-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db3b8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3b8-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db3b8-145">INPUTS</span></span>

### <span data-ttu-id="db3b8-146">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="db3b8-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="db3b8-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db3b8-147">OUTPUTS</span></span>

### <span data-ttu-id="db3b8-148">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="db3b8-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="db3b8-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db3b8-149">NOTES</span></span>

<span data-ttu-id="db3b8-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="db3b8-150">ALIASES</span></span>

<span data-ttu-id="db3b8-151">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="db3b8-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db3b8-152">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="db3b8-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db3b8-153">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="db3b8-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db3b8-154">IRÁNYÍTÓPULT <IDashboard> : a megosztott irányítópult erőforrás-definíciója.</span><span class="sxs-lookup"><span data-stu-id="db3b8-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="db3b8-155">`Location <String>`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="db3b8-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="db3b8-156">`[Lens <IDashboardPropertiesLenses>]`: Az irányítópult lencséi.</span><span class="sxs-lookup"><span data-stu-id="db3b8-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="db3b8-157">`[(Any) <IDashboardLens>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="db3b8-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="db3b8-158">`[Metadata <IDashboardPropertiesMetadata>]`: Az irányítópult metaadatai.</span><span class="sxs-lookup"><span data-stu-id="db3b8-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="db3b8-159">`[(Any) <Object>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="db3b8-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="db3b8-160">`[Tag <IDashboardTags>]`: Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="db3b8-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="db3b8-161">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="db3b8-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="db3b8-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db3b8-162">RELATED LINKS</span></span>

