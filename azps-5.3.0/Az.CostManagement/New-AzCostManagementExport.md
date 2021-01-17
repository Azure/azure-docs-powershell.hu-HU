---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480509"
---
# <span data-ttu-id="8985a-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="8985a-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="8985a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8985a-102">SYNOPSIS</span></span>
<span data-ttu-id="8985a-103">Az exportálás létrehozására vagy frissítésére vonatkozó művelet.</span><span class="sxs-lookup"><span data-stu-id="8985a-103">The operation to create or update a export.</span></span>
<span data-ttu-id="8985a-104">A frissítési művelethez be kell állítani a legújabb eTag-et a kérelemben.</span><span class="sxs-lookup"><span data-stu-id="8985a-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="8985a-105">A get művelettel beszerezheti a legújabb eTag-et.</span><span class="sxs-lookup"><span data-stu-id="8985a-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="8985a-106">A létrehozási művelethez nincs szükség eTag gombra.</span><span class="sxs-lookup"><span data-stu-id="8985a-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="8985a-107">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8985a-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8985a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8985a-108">DESCRIPTION</span></span>
<span data-ttu-id="8985a-109">Az exportálás létrehozására vagy frissítésére vonatkozó művelet.</span><span class="sxs-lookup"><span data-stu-id="8985a-109">The operation to create or update a export.</span></span>
<span data-ttu-id="8985a-110">A frissítési művelethez be kell állítani a legújabb eTag-et a kérelemben.</span><span class="sxs-lookup"><span data-stu-id="8985a-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="8985a-111">A get művelettel beszerezheti a legújabb eTag-et.</span><span class="sxs-lookup"><span data-stu-id="8985a-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="8985a-112">A létrehozási művelethez nincs szükség eTag gombra.</span><span class="sxs-lookup"><span data-stu-id="8985a-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="8985a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8985a-113">EXAMPLES</span></span>

### <span data-ttu-id="8985a-114">1. példa: AzCostManagementExport létrehozása</span><span class="sxs-lookup"><span data-stu-id="8985a-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="8985a-115">AzCostManagementExport létrehozása</span><span class="sxs-lookup"><span data-stu-id="8985a-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="8985a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8985a-116">PARAMETERS</span></span>

### <span data-ttu-id="8985a-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="8985a-117">-ConfigurationColumn</span></span>
<span data-ttu-id="8985a-118">Az exportálásban szerepeltetniandó oszlopnevek tömbje.</span><span class="sxs-lookup"><span data-stu-id="8985a-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="8985a-119">Ha nincs megtéve, akkor az exportálás az összes elérhető oszlopot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8985a-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="8985a-120">Az elérhető oszlopok az ügyfélcsatornától függően változhatnak (lásd a példákat).</span><span class="sxs-lookup"><span data-stu-id="8985a-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="8985a-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="8985a-121">-DataSetGranularity</span></span>
<span data-ttu-id="8985a-122">Az exportálás sorai részletessége.</span><span class="sxs-lookup"><span data-stu-id="8985a-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="8985a-123">Jelenleg csak a "Naponta" támogatott.</span><span class="sxs-lookup"><span data-stu-id="8985a-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="8985a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8985a-124">-DefaultProfile</span></span>
<span data-ttu-id="8985a-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8985a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8985a-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="8985a-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="8985a-127">Az exportáláshoz szükséges adatok behúzásának időkerete.</span><span class="sxs-lookup"><span data-stu-id="8985a-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="8985a-128">Ha egyéni, akkor meg kell adni egy adott időszakot.</span><span class="sxs-lookup"><span data-stu-id="8985a-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="8985a-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="8985a-129">-DefinitionType</span></span>
<span data-ttu-id="8985a-130">Az exportálás típusa.</span><span class="sxs-lookup"><span data-stu-id="8985a-130">The type of the export.</span></span>
<span data-ttu-id="8985a-131">Felhívjuk a figyelmét arra, hogy a "Usage" (Használat) egyenértékű a "ActualCost" értékekkel, és olyan exportokra alkalmazható, amelyek még nem nyújtanak adatokat a szolgáltatásfoglalások díjára vagy amortizációs összegére.</span><span class="sxs-lookup"><span data-stu-id="8985a-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="8985a-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="8985a-132">-DestinationContainer</span></span>
<span data-ttu-id="8985a-133">Annak a tárolónak a neve, amelybe exportálni fogja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="8985a-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="8985a-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="8985a-134">-DestinationResourceId</span></span>
<span data-ttu-id="8985a-135">Annak a tárfióknak az erőforrás-azonosítója, amelybe exportálni fogják az etikát.</span><span class="sxs-lookup"><span data-stu-id="8985a-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="8985a-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="8985a-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="8985a-137">Annak a könyvtárnak a neve, amelybe az exportálást feltölti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8985a-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="8985a-138">-Format</span><span class="sxs-lookup"><span data-stu-id="8985a-138">-Format</span></span>
<span data-ttu-id="8985a-139">A kézbesített exportálás formátuma.</span><span class="sxs-lookup"><span data-stu-id="8985a-139">The format of the export being delivered.</span></span>
<span data-ttu-id="8985a-140">Jelenleg csak a "Csv" támogatott.</span><span class="sxs-lookup"><span data-stu-id="8985a-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="8985a-141">-Name</span><span class="sxs-lookup"><span data-stu-id="8985a-141">-Name</span></span>
<span data-ttu-id="8985a-142">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="8985a-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="8985a-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="8985a-144">Az ismétlődés kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="8985a-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="8985a-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="8985a-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="8985a-146">Az ismétlődés záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="8985a-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="8985a-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="8985a-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="8985a-148">Az ismétlődés ütemezése.</span><span class="sxs-lookup"><span data-stu-id="8985a-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="8985a-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="8985a-149">-ScheduleStatus</span></span>
<span data-ttu-id="8985a-150">Az exportálás ütemezésének állapota.</span><span class="sxs-lookup"><span data-stu-id="8985a-150">The status of the export's schedule.</span></span>
<span data-ttu-id="8985a-151">Ha "Inaktív" állapotban van, az exportálás ütemezése fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="8985a-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="8985a-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="8985a-152">-Scope</span></span>
<span data-ttu-id="8985a-153">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8985a-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="8985a-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="8985a-154">-TimePeriodFrom</span></span>
<span data-ttu-id="8985a-155">Az adatok exportálásának kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="8985a-155">The start date for export data.</span></span>

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

### <span data-ttu-id="8985a-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="8985a-156">-TimePeriodTo</span></span>
<span data-ttu-id="8985a-157">Az adatok exportálásának záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="8985a-157">The end date for export data.</span></span>

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

### <span data-ttu-id="8985a-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8985a-158">-Confirm</span></span>
<span data-ttu-id="8985a-159">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8985a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8985a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8985a-160">-WhatIf</span></span>
<span data-ttu-id="8985a-161">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8985a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8985a-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8985a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8985a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8985a-163">CommonParameters</span></span>
<span data-ttu-id="8985a-164">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8985a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8985a-165">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8985a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8985a-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8985a-166">INPUTS</span></span>

## <span data-ttu-id="8985a-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8985a-167">OUTPUTS</span></span>

### <span data-ttu-id="8985a-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="8985a-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="8985a-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8985a-169">NOTES</span></span>

<span data-ttu-id="8985a-170">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8985a-170">ALIASES</span></span>

## <span data-ttu-id="8985a-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8985a-171">RELATED LINKS</span></span>

