---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184272"
---
# <span data-ttu-id="6cefb-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="6cefb-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="6cefb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cefb-102">SYNOPSIS</span></span>
<span data-ttu-id="6cefb-103">Meglévő irányítópult frissítése</span><span class="sxs-lookup"><span data-stu-id="6cefb-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="6cefb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cefb-104">SYNTAX</span></span>

### <span data-ttu-id="6cefb-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cefb-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6cefb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6cefb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cefb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cefb-107">DESCRIPTION</span></span>
<span data-ttu-id="6cefb-108">Meglévő irányítópult frissítése</span><span class="sxs-lookup"><span data-stu-id="6cefb-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="6cefb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6cefb-109">EXAMPLES</span></span>

### <span data-ttu-id="6cefb-110">1. példa: az irányítópultok címkéit frissíti</span><span class="sxs-lookup"><span data-stu-id="6cefb-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="6cefb-111">A címkék frissítése az irányítópulton</span><span class="sxs-lookup"><span data-stu-id="6cefb-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="6cefb-112">A címkéket a program szövegközi Hashtable jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6cefb-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="6cefb-113">2. példa: az irányítópult-címkék frissítése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="6cefb-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="6cefb-114">Frissítheti az irányítópultok címkéit a Get-AzPortalDashboard használatával.</span><span class="sxs-lookup"><span data-stu-id="6cefb-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="6cefb-115">Ezt a lehetőséget használva frissítheti a címkéket egyetlen irányítópulton vagy több dashboardfs is.</span><span class="sxs-lookup"><span data-stu-id="6cefb-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="6cefb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cefb-116">PARAMETERS</span></span>

### <span data-ttu-id="6cefb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cefb-117">-DefaultProfile</span></span>
<span data-ttu-id="6cefb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cefb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cefb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cefb-119">-InputObject</span></span>
<span data-ttu-id="6cefb-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6cefb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6cefb-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="6cefb-121">-Lens</span></span>
<span data-ttu-id="6cefb-122">Az irányítópult lencséi.</span><span class="sxs-lookup"><span data-stu-id="6cefb-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="6cefb-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6cefb-123">-Metadata</span></span>
<span data-ttu-id="6cefb-124">Az irányítópult metaadatai.</span><span class="sxs-lookup"><span data-stu-id="6cefb-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="6cefb-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cefb-125">-Name</span></span>
<span data-ttu-id="6cefb-126">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="6cefb-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="6cefb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cefb-127">-ResourceGroupName</span></span>
<span data-ttu-id="6cefb-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cefb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cefb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cefb-129">-SubscriptionId</span></span>
<span data-ttu-id="6cefb-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cefb-130">The Azure subscription ID.</span></span>
<span data-ttu-id="6cefb-131">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6cefb-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6cefb-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="6cefb-132">-Tag</span></span>
<span data-ttu-id="6cefb-133">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="6cefb-133">Resource tags</span></span>

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

### <span data-ttu-id="6cefb-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cefb-134">-Confirm</span></span>
<span data-ttu-id="6cefb-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cefb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cefb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cefb-136">-WhatIf</span></span>
<span data-ttu-id="6cefb-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cefb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cefb-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cefb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cefb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cefb-139">CommonParameters</span></span>
<span data-ttu-id="6cefb-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cefb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cefb-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6cefb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cefb-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cefb-142">INPUTS</span></span>

### <span data-ttu-id="6cefb-143">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="6cefb-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="6cefb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cefb-144">OUTPUTS</span></span>

### <span data-ttu-id="6cefb-145">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="6cefb-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="6cefb-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cefb-146">NOTES</span></span>

<span data-ttu-id="6cefb-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6cefb-147">ALIASES</span></span>

<span data-ttu-id="6cefb-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6cefb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cefb-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6cefb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cefb-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6cefb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cefb-151">INPUTOBJECT <IPortalIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6cefb-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cefb-152">`[DashboardName <String>]`: Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="6cefb-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="6cefb-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6cefb-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cefb-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cefb-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6cefb-155">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cefb-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6cefb-156">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6cefb-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6cefb-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cefb-157">RELATED LINKS</span></span>

