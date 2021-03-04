---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: d4be10cf33952b026ceabe6cd407929acbe5c058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918986"
---
# <span data-ttu-id="99143-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="99143-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="99143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99143-102">SYNOPSIS</span></span>
<span data-ttu-id="99143-103">Az exportálás létrehozására vagy frissítésére vonatkozó művelet.</span><span class="sxs-lookup"><span data-stu-id="99143-103">The operation to create or update a export.</span></span>
<span data-ttu-id="99143-104">A frissítési művelethez be kell állítani a legújabb eTag-et a kérelemben.</span><span class="sxs-lookup"><span data-stu-id="99143-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="99143-105">A get művelettel beszerezheti a legújabb eTag-et.</span><span class="sxs-lookup"><span data-stu-id="99143-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="99143-106">A létrehozási művelethez nincs szükség eTag gombra.</span><span class="sxs-lookup"><span data-stu-id="99143-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="99143-107">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99143-107">SYNTAX</span></span>

### <span data-ttu-id="99143-108">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99143-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99143-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="99143-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99143-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99143-110">DESCRIPTION</span></span>
<span data-ttu-id="99143-111">Az exportálás létrehozására vagy frissítésére vonatkozó művelet.</span><span class="sxs-lookup"><span data-stu-id="99143-111">The operation to create or update a export.</span></span>
<span data-ttu-id="99143-112">A frissítési művelethez be kell állítani a legújabb eTag-et a kérelemben.</span><span class="sxs-lookup"><span data-stu-id="99143-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="99143-113">A get művelettel beszerezheti a legújabb eTag-et.</span><span class="sxs-lookup"><span data-stu-id="99143-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="99143-114">A létrehozási művelethez nincs szükség eTag gombra.</span><span class="sxs-lookup"><span data-stu-id="99143-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="99143-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99143-115">EXAMPLES</span></span>

### <span data-ttu-id="99143-116">1. példa: AzCostManagementExport frissítése hatókör és név szerint</span><span class="sxs-lookup"><span data-stu-id="99143-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="99143-117">Update AzCostManagementExport by Scope and name</span><span class="sxs-lookup"><span data-stu-id="99143-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="99143-118">2. példa: AzCostManagementExport frissítése inputObject szerint</span><span class="sxs-lookup"><span data-stu-id="99143-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="99143-119">Update AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="99143-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="99143-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99143-120">PARAMETERS</span></span>

### <span data-ttu-id="99143-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="99143-121">-ConfigurationColumn</span></span>
<span data-ttu-id="99143-122">Az exportálásban szerepeltetniandó oszlopnevek tömbje.</span><span class="sxs-lookup"><span data-stu-id="99143-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="99143-123">Ha nincs megtéve, akkor az exportálás az összes elérhető oszlopot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="99143-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="99143-124">Az elérhető oszlopok az ügyfélcsatornától függően változhatnak (lásd a példákat).</span><span class="sxs-lookup"><span data-stu-id="99143-124">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="99143-125">-DataSetGranularity</span></span>
<span data-ttu-id="99143-126">Az exportálás sorai részletessége.</span><span class="sxs-lookup"><span data-stu-id="99143-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="99143-127">Jelenleg csak a "Naponta" támogatott.</span><span class="sxs-lookup"><span data-stu-id="99143-127">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99143-128">-DefaultProfile</span></span>
<span data-ttu-id="99143-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99143-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99143-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="99143-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="99143-131">Az exportáláshoz szükséges adatok behúzásának időkerete.</span><span class="sxs-lookup"><span data-stu-id="99143-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="99143-132">Ha egyéni, akkor meg kell adni egy adott időszakot.</span><span class="sxs-lookup"><span data-stu-id="99143-132">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="99143-133">-DefinitionType</span></span>
<span data-ttu-id="99143-134">Az exportálás típusa.</span><span class="sxs-lookup"><span data-stu-id="99143-134">The type of the export.</span></span>
<span data-ttu-id="99143-135">Felhívjuk a figyelmét arra, hogy a "Usage" (Használat) egyenértékű a "ActualCost" értékekkel, és olyan exportokra alkalmazható, amelyek még nem szolgáltatnak adatokat a szolgáltatásfoglalások díjára vagy amortizációs összegére.</span><span class="sxs-lookup"><span data-stu-id="99143-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="99143-136">-DestinationContainer</span></span>
<span data-ttu-id="99143-137">Annak a tárolónak a neve, amelybe exportálni fogja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="99143-137">The name of the container where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="99143-138">-DestinationResourceId</span></span>
<span data-ttu-id="99143-139">Annak a tárfióknak az erőforrás-azonosítója, amelybe exportálni fogják az etikát.</span><span class="sxs-lookup"><span data-stu-id="99143-139">The resource id of the storage account where exports will be delivered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="99143-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="99143-141">Annak a könyvtárnak a neve, amelybe az exportálást feltölti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="99143-141">The name of the directory where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="99143-142">-ETag</span></span>
<span data-ttu-id="99143-143">Az erőforrás eTagja.</span><span class="sxs-lookup"><span data-stu-id="99143-143">eTag of the resource.</span></span>
<span data-ttu-id="99143-144">Az egyidejű frissítési esetek kezeléséhez ez a mező határozza meg, hogy a felhasználó frissíti-e a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="99143-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-145">-Format</span><span class="sxs-lookup"><span data-stu-id="99143-145">-Format</span></span>
<span data-ttu-id="99143-146">A kézbesített exportálás formátuma.</span><span class="sxs-lookup"><span data-stu-id="99143-146">The format of the export being delivered.</span></span>
<span data-ttu-id="99143-147">Jelenleg csak a "Csv" támogatott.</span><span class="sxs-lookup"><span data-stu-id="99143-147">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99143-148">-InputObject</span></span>
<span data-ttu-id="99143-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="99143-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99143-150">-Name</span><span class="sxs-lookup"><span data-stu-id="99143-150">-Name</span></span>
<span data-ttu-id="99143-151">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="99143-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="99143-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="99143-153">Az ismétlődés kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="99143-153">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="99143-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="99143-155">Az ismétlődés záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="99143-155">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="99143-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="99143-157">Az ismétlődés ütemezése.</span><span class="sxs-lookup"><span data-stu-id="99143-157">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="99143-158">-ScheduleStatus</span></span>
<span data-ttu-id="99143-159">Az exportálás ütemezésének állapota.</span><span class="sxs-lookup"><span data-stu-id="99143-159">The status of the export's schedule.</span></span>
<span data-ttu-id="99143-160">Ha "Inaktív" állapotban van, az exportálás ütemezése fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="99143-160">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="99143-161">-Scope</span></span>
<span data-ttu-id="99143-162">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="99143-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="99143-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="99143-163">-TimePeriodFrom</span></span>
<span data-ttu-id="99143-164">Az adatok exportálásának kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="99143-164">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="99143-165">-TimePeriodTo</span></span>
<span data-ttu-id="99143-166">Az adatok exportálásának záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="99143-166">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99143-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99143-167">-Confirm</span></span>
<span data-ttu-id="99143-168">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="99143-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99143-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99143-169">-WhatIf</span></span>
<span data-ttu-id="99143-170">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="99143-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99143-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99143-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99143-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99143-172">CommonParameters</span></span>
<span data-ttu-id="99143-173">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99143-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99143-174">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99143-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99143-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99143-175">INPUTS</span></span>

### <span data-ttu-id="99143-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="99143-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="99143-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99143-177">OUTPUTS</span></span>

### <span data-ttu-id="99143-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="99143-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="99143-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99143-179">NOTES</span></span>

<span data-ttu-id="99143-180">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="99143-180">ALIASES</span></span>

<span data-ttu-id="99143-181">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="99143-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99143-182">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="99143-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99143-183">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99143-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99143-184">INPUTOBJECT: <ICostManagementIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="99143-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99143-185">`[AlertId <String>]`: Riasztásazonosító</span><span class="sxs-lookup"><span data-stu-id="99143-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="99143-186">`[ExportName <String>]`: Export Name.</span><span class="sxs-lookup"><span data-stu-id="99143-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="99143-187">`[ExternalCloudProviderId <String>]`: Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="99143-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="99143-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: A dimenzióval/lekérdezéssel kapcsolatos műveletekhez társított külső felhőszolgáltató típusa.</span><span class="sxs-lookup"><span data-stu-id="99143-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="99143-189">Ide tartozik az összekapcsolt fiók "külsőSubscriptions" és a "externalBillingAccounts" az összesített fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="99143-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="99143-190">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="99143-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99143-191">`[Scope <String>]`: A nézetműveletekkel társított hatókör.</span><span class="sxs-lookup"><span data-stu-id="99143-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="99143-192">Ide tartozik az "előfizetések/{subscriptionId}" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' a Számlázási fiók hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" a EnrollmentAccount hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' a Felügyeleti csoport hatóköréhez, "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" külső számlázási fiók hatóköréhez és a "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" külső előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="99143-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="99143-193">`[ViewName <String>]`: Nézet neve</span><span class="sxs-lookup"><span data-stu-id="99143-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="99143-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99143-194">RELATED LINKS</span></span>

