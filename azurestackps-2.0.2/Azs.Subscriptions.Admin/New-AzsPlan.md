---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017084"
---
# <span data-ttu-id="ed9d6-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="ed9d6-101">New-AzsPlan</span></span>

## <span data-ttu-id="ed9d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9d6-103">Hozza létre vagy frissítse a csomagot.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-103">Create or update the plan.</span></span>

## <span data-ttu-id="ed9d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed9d6-104">SYNTAX</span></span>

### <span data-ttu-id="ed9d6-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed9d6-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed9d6-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="ed9d6-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed9d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed9d6-107">DESCRIPTION</span></span>
<span data-ttu-id="ed9d6-108">Hozza létre vagy frissítse a csomagot.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-108">Create or update the plan.</span></span>

## <span data-ttu-id="ed9d6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ed9d6-109">EXAMPLES</span></span>

### <span data-ttu-id="ed9d6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed9d6-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="ed9d6-111">Új csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="ed9d6-111">Creates a new plan</span></span>

## <span data-ttu-id="ed9d6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed9d6-112">PARAMETERS</span></span>

### <span data-ttu-id="ed9d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9d6-113">-DefaultProfile</span></span>
<span data-ttu-id="ed9d6-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9d6-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ed9d6-115">-Description</span></span>
<span data-ttu-id="ed9d6-116">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed9d6-117">-DisplayName</span></span>
<span data-ttu-id="ed9d6-118">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="ed9d6-119">-ExternalReferenceId</span></span>
<span data-ttu-id="ed9d6-120">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="ed9d6-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="ed9d6-121">-Location</span></span>
<span data-ttu-id="ed9d6-122">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="ed9d6-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed9d6-123">-Name</span></span>
<span data-ttu-id="ed9d6-124">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-124">Name of the plan.</span></span>

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

### <span data-ttu-id="ed9d6-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="ed9d6-125">-PlanDefinition</span></span>
<span data-ttu-id="ed9d6-126">A terv az olyan kvóták és funkciók csomagját jelenti, amelyek a bérlők számára elérhetők.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="ed9d6-127">A bérlő ezt a csomagot egy ajánlaton keresztül is megszerezheti, és a Felhőbeli szolgáltatásokhoz való hozzáférését frissítheti.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="ed9d6-128">A kivitelezéshez tekintse meg a PLANDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-129">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="ed9d6-129">-PropertiesName</span></span>
<span data-ttu-id="ed9d6-130">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="ed9d6-131">-QuotaIds</span></span>
<span data-ttu-id="ed9d6-132">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9d6-133">-ResourceGroupName</span></span>
<span data-ttu-id="ed9d6-134">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ed9d6-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="ed9d6-135">-SkuIds</span></span>
<span data-ttu-id="ed9d6-136">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="ed9d6-137">-SubscriptionCount</span></span>
<span data-ttu-id="ed9d6-138">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="ed9d6-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ed9d6-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed9d6-139">-SubscriptionId</span></span>
<span data-ttu-id="ed9d6-140">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ed9d6-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed9d6-141">-Confirm</span></span>
<span data-ttu-id="ed9d6-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed9d6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed9d6-143">-WhatIf</span></span>
<span data-ttu-id="ed9d6-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9d6-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed9d6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9d6-146">CommonParameters</span></span>
<span data-ttu-id="ed9d6-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed9d6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9d6-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9d6-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed9d6-149">INPUTS</span></span>

### <span data-ttu-id="ed9d6-150">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="ed9d6-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="ed9d6-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed9d6-151">OUTPUTS</span></span>

### <span data-ttu-id="ed9d6-152">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="ed9d6-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="ed9d6-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ed9d6-153">ALIASES</span></span>

## <span data-ttu-id="ed9d6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed9d6-154">NOTES</span></span>

<span data-ttu-id="ed9d6-155">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed9d6-156">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ed9d6-157">PLANDEFINITION <IPlan> : a terv olyan kvóták és funkciók csomagját jelöli, amelyek a bérlők számára elérhetők.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="ed9d6-158">A bérlő ezt a csomagot egy ajánlaton keresztül is megszerezheti, és a Felhőbeli szolgáltatásokhoz való hozzáférését frissítheti.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="ed9d6-159">`[Location <String>]`: Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="ed9d6-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="ed9d6-160">`[Description <String>]`: A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="ed9d6-161">`[DisplayName <String>]`: Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="ed9d6-162">`[ExternalReferenceId <String>]`: Külső hivatkozási azonosító.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="ed9d6-163">`[PropertiesName <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="ed9d6-164">`[QuotaIds <String[]>]`: A terv szerinti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="ed9d6-165">`[SkuIds <String[]>]`: SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="ed9d6-166">`[SubscriptionCount <Int32?>]`: Előfizetés száma.</span><span class="sxs-lookup"><span data-stu-id="ed9d6-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="ed9d6-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed9d6-167">RELATED LINKS</span></span>

