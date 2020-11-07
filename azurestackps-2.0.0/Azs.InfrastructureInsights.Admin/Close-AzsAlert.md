---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842573"
---
# <span data-ttu-id="7baa1-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="7baa1-101">Close-AzsAlert</span></span>

## <span data-ttu-id="7baa1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7baa1-102">SYNOPSIS</span></span>
<span data-ttu-id="7baa1-103">Bezárja az adott riasztást.</span><span class="sxs-lookup"><span data-stu-id="7baa1-103">Closes the given alert.</span></span>

## <span data-ttu-id="7baa1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7baa1-104">SYNTAX</span></span>

### <span data-ttu-id="7baa1-105">CloseExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7baa1-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7baa1-106">Zárja be</span><span class="sxs-lookup"><span data-stu-id="7baa1-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7baa1-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7baa1-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7baa1-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7baa1-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7baa1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7baa1-109">DESCRIPTION</span></span>
<span data-ttu-id="7baa1-110">Bezárja az adott riasztást.</span><span class="sxs-lookup"><span data-stu-id="7baa1-110">Closes the given alert.</span></span>

## <span data-ttu-id="7baa1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7baa1-111">EXAMPLES</span></span>

### <span data-ttu-id="7baa1-112">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="7baa1-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="7baa1-113">Riasztás megszüntetése név szerint</span><span class="sxs-lookup"><span data-stu-id="7baa1-113">Close an alert by Name.</span></span>

### <span data-ttu-id="7baa1-114">2. példa:</span><span class="sxs-lookup"><span data-stu-id="7baa1-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="7baa1-115">Riasztást az adatcsöveken keresztül zárhatja be.</span><span class="sxs-lookup"><span data-stu-id="7baa1-115">Close an alert through piping.</span></span>

## <span data-ttu-id="7baa1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7baa1-116">PARAMETERS</span></span>

### <span data-ttu-id="7baa1-117">-Értesítés</span><span class="sxs-lookup"><span data-stu-id="7baa1-117">-Alert</span></span>
<span data-ttu-id="7baa1-118">Ez az objektum egy riasztási erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7baa1-118">This object represents an alert resource.</span></span>
<span data-ttu-id="7baa1-119">A kivitelezéshez tekintse meg az ÉRTESÍTÉSi tulajdonságok című szakaszt, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7baa1-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="7baa1-120">-AlertId</span></span>
<span data-ttu-id="7baa1-121">Megkapja vagy beállítja a riasztás AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="7baa1-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="7baa1-122">-AlertProperty</span></span>
<span data-ttu-id="7baa1-123">A riasztás tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="7baa1-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="7baa1-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="7baa1-125">Az a felhasználó aliasneve, aki bezárta az értesítést.</span><span class="sxs-lookup"><span data-stu-id="7baa1-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="7baa1-126">-ClosedTimestamp</span></span>
<span data-ttu-id="7baa1-127">Időbélyegző a riasztás lezárásakor.</span><span class="sxs-lookup"><span data-stu-id="7baa1-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="7baa1-128">-CreatedTimestamp</span></span>
<span data-ttu-id="7baa1-129">Időbélyegző a riasztás létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="7baa1-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baa1-130">-DefaultProfile</span></span>
<span data-ttu-id="7baa1-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7baa1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7baa1-132">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7baa1-132">-Description</span></span>
<span data-ttu-id="7baa1-133">A riasztás leírása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="7baa1-134">-FaultId</span></span>
<span data-ttu-id="7baa1-135">Megkapja vagy beállítja a riasztás hibájának AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="7baa1-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="7baa1-136">-FaultTypeId</span></span>
<span data-ttu-id="7baa1-137">A riasztás hibájának típusa AZONOSÍTÓját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="7baa1-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="7baa1-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="7baa1-139">Azt jelzi, hogy a riasztás visszaközvetíthető-e.</span><span class="sxs-lookup"><span data-stu-id="7baa1-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="7baa1-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="7baa1-141">Az érintett elem megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="7baa1-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="7baa1-142">-ImpactedResourceId</span></span>
<span data-ttu-id="7baa1-143">Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7baa1-144">-InputObject</span></span>
<span data-ttu-id="7baa1-145">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7baa1-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="7baa1-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="7baa1-147">Időbélyegző a riasztás utolsó frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="7baa1-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-148">-Hely</span><span class="sxs-lookup"><span data-stu-id="7baa1-148">-Location</span></span>
<span data-ttu-id="7baa1-149">A régió neve</span><span class="sxs-lookup"><span data-stu-id="7baa1-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="7baa1-150">-Location1</span></span>
<span data-ttu-id="7baa1-151">Az az Azure-terület, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="7baa1-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7baa1-152">-Name</span></span>
<span data-ttu-id="7baa1-153">A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="7baa1-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-154">-Kármentesítés</span><span class="sxs-lookup"><span data-stu-id="7baa1-154">-Remediation</span></span>
<span data-ttu-id="7baa1-155">Beolvassa vagy beállítja a riasztáshoz szükséges rendszergazdai szervizelési utasításokat.</span><span class="sxs-lookup"><span data-stu-id="7baa1-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7baa1-156">-ResourceGroupName</span></span>
<span data-ttu-id="7baa1-157">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7baa1-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="7baa1-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="7baa1-159">Megkapja vagy beállítja annak a szolgáltatásnak a regisztrációs AZONOSÍTÓját, amelyre a riasztás tartozik.</span><span class="sxs-lookup"><span data-stu-id="7baa1-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="7baa1-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="7baa1-161">A riasztáshoz társított erőforrás regisztrációs AZONOSÍTÓjának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="7baa1-162">Ha a riasztás nincs erőforráshoz társítva, az erőforrás-regisztrációs azonosító értéke null.</span><span class="sxs-lookup"><span data-stu-id="7baa1-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-163">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="7baa1-163">-Severity</span></span>
<span data-ttu-id="7baa1-164">A riasztás súlyossága.</span><span class="sxs-lookup"><span data-stu-id="7baa1-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-165">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="7baa1-165">-State</span></span>
<span data-ttu-id="7baa1-166">A riasztás állapota</span><span class="sxs-lookup"><span data-stu-id="7baa1-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7baa1-167">-SubscriptionId</span></span>
<span data-ttu-id="7baa1-168">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="7baa1-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7baa1-169">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7baa1-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-170">-Címke</span><span class="sxs-lookup"><span data-stu-id="7baa1-170">-Tag</span></span>
<span data-ttu-id="7baa1-171">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="7baa1-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-172">-Cím</span><span class="sxs-lookup"><span data-stu-id="7baa1-172">-Title</span></span>
<span data-ttu-id="7baa1-173">Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7baa1-174">-Felhasználó</span><span class="sxs-lookup"><span data-stu-id="7baa1-174">-User</span></span>
<span data-ttu-id="7baa1-175">A művelet végrehajtásához használt Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="7baa1-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="7baa1-176">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7baa1-176">-Confirm</span></span>
<span data-ttu-id="7baa1-177">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7baa1-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7baa1-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7baa1-178">-WhatIf</span></span>
<span data-ttu-id="7baa1-179">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7baa1-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7baa1-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7baa1-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7baa1-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baa1-181">CommonParameters</span></span>
<span data-ttu-id="7baa1-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7baa1-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baa1-183">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7baa1-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baa1-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7baa1-184">INPUTS</span></span>

### <span data-ttu-id="7baa1-185">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="7baa1-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="7baa1-186">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7baa1-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="7baa1-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7baa1-187">OUTPUTS</span></span>

### <span data-ttu-id="7baa1-188">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="7baa1-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="7baa1-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7baa1-189">NOTES</span></span>

<span data-ttu-id="7baa1-190">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7baa1-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7baa1-191">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7baa1-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7baa1-192">RIASZTÁS <IAlert> : ez az objektum egy riasztási erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7baa1-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="7baa1-193">`[Location <String>]`: Az Azure régió, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="7baa1-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="7baa1-194">`[Tag <ITrackedResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="7baa1-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="7baa1-195">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="7baa1-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7baa1-196">`[AlertId <String>]`: Beolvassa vagy beállítja a riasztás AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="7baa1-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="7baa1-197">`[AlertProperty <IAlertModelAlertProperties>]`: A riasztás tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="7baa1-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="7baa1-198">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="7baa1-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7baa1-199">`[ClosedByUserAlias <String>]`: Az a felhasználó aliasneve, aki bezárta az értesítést.</span><span class="sxs-lookup"><span data-stu-id="7baa1-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="7baa1-200">`[ClosedTimestamp <String>]`: Időbélyegző, ha a riasztás be van zárva.</span><span class="sxs-lookup"><span data-stu-id="7baa1-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="7baa1-201">`[CreatedTimestamp <String>]`: Időbélyegző a riasztás létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="7baa1-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="7baa1-202">`[Description <IDictionary[]>]`: A riasztás leírása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="7baa1-203">`[FaultId <String>]`: Beolvassa vagy beállítja a riasztás hibájának AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="7baa1-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="7baa1-204">`[FaultTypeId <String>]`: Beolvassa vagy beállítja a riasztás hibájának típusát AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="7baa1-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="7baa1-205">`[HasValidRemediationAction <Boolean?>]`: Azt jelzi, hogy a riasztás visszaközvetíthető-e.</span><span class="sxs-lookup"><span data-stu-id="7baa1-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="7baa1-206">`[ImpactedResourceDisplayName <String>]`: Az ütközésben lévő elem megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="7baa1-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="7baa1-207">`[ImpactedResourceId <String>]`: Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="7baa1-208">`[LastUpdatedTimestamp <String>]`: Időbélyegző a riasztás utolsó frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="7baa1-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="7baa1-209">`[Remediation <IDictionary[]>]`: A riasztáshoz beolvassa vagy beállítja a rendszergazdai felhasználóbarát szervizelési utasításokat.</span><span class="sxs-lookup"><span data-stu-id="7baa1-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="7baa1-210">`[ResourceProviderRegistrationId <String>]`: Beadja vagy beállítja annak a szolgáltatásnak a regisztrációs AZONOSÍTÓját, amelyre a riasztás tartozik.</span><span class="sxs-lookup"><span data-stu-id="7baa1-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="7baa1-211">`[ResourceRegistrationId <String>]`: A riasztáshoz társított erőforrás regisztrációs AZONOSÍTÓjának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="7baa1-212">Ha a riasztás nincs erőforráshoz társítva, az erőforrás-regisztrációs azonosító értéke null.</span><span class="sxs-lookup"><span data-stu-id="7baa1-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="7baa1-213">`[Severity <String>]`: A riasztás súlyossága.</span><span class="sxs-lookup"><span data-stu-id="7baa1-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="7baa1-214">`[State <String>]`: A riasztás állapota.</span><span class="sxs-lookup"><span data-stu-id="7baa1-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="7baa1-215">`[Title <String>]`: Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="7baa1-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="7baa1-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="7baa1-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7baa1-217">`[AlertName <String>]`: A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="7baa1-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="7baa1-218">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7baa1-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7baa1-219">`[Location <String>]`: A régió neve</span><span class="sxs-lookup"><span data-stu-id="7baa1-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="7baa1-220">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7baa1-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7baa1-221">`[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="7baa1-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="7baa1-222">`[ServiceHealth <String>]`: Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="7baa1-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="7baa1-223">`[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="7baa1-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="7baa1-224">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="7baa1-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7baa1-225">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7baa1-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7baa1-226">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7baa1-226">RELATED LINKS</span></span>

