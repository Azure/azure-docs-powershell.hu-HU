---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151251"
---
# <span data-ttu-id="2ebd3-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="2ebd3-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="2ebd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ebd3-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebd3-103">Egy meglévő irányítópult frissítése.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="2ebd3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ebd3-104">SYNTAX</span></span>

### <span data-ttu-id="2ebd3-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ebd3-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ebd3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2ebd3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ebd3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ebd3-107">DESCRIPTION</span></span>
<span data-ttu-id="2ebd3-108">Egy meglévő irányítópult frissítése.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="2ebd3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ebd3-109">EXAMPLES</span></span>

### <span data-ttu-id="2ebd3-110">1. példa: Irányítópult címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="2ebd3-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="2ebd3-111">Frissítse a címkéket az irányítópulton.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="2ebd3-112">A címkék beágyazott hashtable-ként vannak ábrázolva.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="2ebd3-113">2. példa: Irányítópult-címkék frissítése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="2ebd3-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="2ebd3-114">Frissítse a Get-AzPortalDashboard használatával újrakért irányítópult címkéit.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="2ebd3-115">Ezzel frissítheti a címkéket egyetlen irányítópulton vagy több irányítópulton keresztül.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="2ebd3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ebd3-116">PARAMETERS</span></span>

### <span data-ttu-id="2ebd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebd3-117">-DefaultProfile</span></span>
<span data-ttu-id="2ebd3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebd3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ebd3-119">-InputObject</span></span>
<span data-ttu-id="2ebd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="2ebd3-121">-Lens</span></span>
<span data-ttu-id="2ebd3-122">Az irányítópult lenjei.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-122">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2ebd3-123">-Metadata</span></span>
<span data-ttu-id="2ebd3-124">Az irányítópult metaadatai.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-124">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2ebd3-125">-Name</span></span>
<span data-ttu-id="2ebd3-126">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebd3-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ebd3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ebd3-129">-SubscriptionId</span></span>
<span data-ttu-id="2ebd3-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-130">The Azure subscription ID.</span></span>
<span data-ttu-id="2ebd3-131">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="2ebd3-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ebd3-132">-Tag</span></span>
<span data-ttu-id="2ebd3-133">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="2ebd3-133">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebd3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ebd3-134">-Confirm</span></span>
<span data-ttu-id="2ebd3-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ebd3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebd3-136">-WhatIf</span></span>
<span data-ttu-id="2ebd3-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ebd3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ebd3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebd3-139">CommonParameters</span></span>
<span data-ttu-id="2ebd3-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebd3-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ebd3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebd3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ebd3-142">INPUTS</span></span>

### <span data-ttu-id="2ebd3-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="2ebd3-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="2ebd3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ebd3-144">OUTPUTS</span></span>

### <span data-ttu-id="2ebd3-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="2ebd3-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="2ebd3-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ebd3-146">NOTES</span></span>

<span data-ttu-id="2ebd3-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2ebd3-147">ALIASES</span></span>

<span data-ttu-id="2ebd3-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2ebd3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ebd3-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ebd3-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ebd3-151">INPUTOBJECT: <IPortalIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2ebd3-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ebd3-152">`[DashboardName <String>]`: Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="2ebd3-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2ebd3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ebd3-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2ebd3-155">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2ebd3-156">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="2ebd3-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2ebd3-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ebd3-157">RELATED LINKS</span></span>

