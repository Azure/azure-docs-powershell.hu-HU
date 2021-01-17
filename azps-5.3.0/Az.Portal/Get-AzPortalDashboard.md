---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384536"
---
# <span data-ttu-id="ad6ac-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="ad6ac-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="ad6ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6ac-103">Az irányítópultot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="ad6ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad6ac-104">SYNTAX</span></span>

### <span data-ttu-id="ad6ac-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad6ac-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad6ac-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ad6ac-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad6ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad6ac-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad6ac-108">Lista</span><span class="sxs-lookup"><span data-stu-id="ad6ac-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad6ac-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad6ac-109">DESCRIPTION</span></span>
<span data-ttu-id="ad6ac-110">Az irányítópultot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="ad6ac-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad6ac-111">EXAMPLES</span></span>

### <span data-ttu-id="ad6ac-112">1. példa: Előfizetés összes irányítópultjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="ad6ac-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="ad6ac-113">Előfizetés összes irányítópultjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="ad6ac-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="ad6ac-114">2. példa: Egyetlen portál irányítópultjának részletei</span><span class="sxs-lookup"><span data-stu-id="ad6ac-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="ad6ac-115">Egyetlen irányítópult részleteinek megtekintése</span><span class="sxs-lookup"><span data-stu-id="ad6ac-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="ad6ac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad6ac-116">PARAMETERS</span></span>

### <span data-ttu-id="ad6ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6ac-117">-DefaultProfile</span></span>
<span data-ttu-id="ad6ac-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad6ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad6ac-119">-InputObject</span></span>
<span data-ttu-id="ad6ac-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad6ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ad6ac-121">-Name</span></span>
<span data-ttu-id="ad6ac-122">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad6ac-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6ac-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad6ac-125">-SubscriptionId</span></span>
<span data-ttu-id="ad6ac-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-126">The Azure subscription ID.</span></span>
<span data-ttu-id="ad6ac-127">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="ad6ac-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6ac-128">CommonParameters</span></span>
<span data-ttu-id="ad6ac-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6ac-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad6ac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6ac-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad6ac-131">INPUTS</span></span>

### <span data-ttu-id="ad6ac-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="ad6ac-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="ad6ac-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad6ac-133">OUTPUTS</span></span>

### <span data-ttu-id="ad6ac-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="ad6ac-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="ad6ac-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad6ac-135">NOTES</span></span>

<span data-ttu-id="ad6ac-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ad6ac-136">ALIASES</span></span>

<span data-ttu-id="ad6ac-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ad6ac-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad6ac-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad6ac-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad6ac-140">INPUTOBJECT: <IPortalIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ad6ac-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad6ac-141">`[DashboardName <String>]`: Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="ad6ac-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ad6ac-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad6ac-143">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ad6ac-144">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad6ac-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ad6ac-145">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="ad6ac-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ad6ac-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad6ac-146">RELATED LINKS</span></span>

