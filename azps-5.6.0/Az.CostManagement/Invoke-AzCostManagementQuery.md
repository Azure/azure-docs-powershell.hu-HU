---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: c1bc78747807d0f481c35fc75ff6fcfc80a83787
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929057"
---
# <span data-ttu-id="26d8a-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="26d8a-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="26d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="26d8a-103">Lekérdezi a hatókör használati adatait.</span><span class="sxs-lookup"><span data-stu-id="26d8a-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="26d8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26d8a-104">SYNTAX</span></span>

### <span data-ttu-id="26d8a-105">UsageExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26d8a-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26d8a-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="26d8a-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26d8a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26d8a-107">DESCRIPTION</span></span>
<span data-ttu-id="26d8a-108">Lekérdezi a hatókör használati adatait.</span><span class="sxs-lookup"><span data-stu-id="26d8a-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="26d8a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26d8a-109">EXAMPLES</span></span>

### <span data-ttu-id="26d8a-110">1. példa: AzCostManagementQuery meghívása hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="26d8a-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="26d8a-111">AzCostManagementQuery meghívása hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="26d8a-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="26d8a-112">2. példa: AzCostManagementQuery meghívása hatókör szerint dimenziókkal</span><span class="sxs-lookup"><span data-stu-id="26d8a-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="26d8a-113">Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="26d8a-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="26d8a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26d8a-114">PARAMETERS</span></span>

### <span data-ttu-id="26d8a-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="26d8a-115">-ConfigurationColumn</span></span>
<span data-ttu-id="26d8a-116">A lekérdezésben szerepeltethető oszlopnevek tömbje.</span><span class="sxs-lookup"><span data-stu-id="26d8a-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="26d8a-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="26d8a-117">-DatasetAggregation</span></span>
<span data-ttu-id="26d8a-118">A lekérdezésben használható összegzési kifejezés szótára.</span><span class="sxs-lookup"><span data-stu-id="26d8a-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="26d8a-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="26d8a-119">-DatasetFilter</span></span>
<span data-ttu-id="26d8a-120">A lekérdezésben használható szűrőkifejezés.</span><span class="sxs-lookup"><span data-stu-id="26d8a-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="26d8a-121">Ennek létrehozásáról a DATASETFILTER tulajdonságairól és a kivonattáblák létrehozásáról a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="26d8a-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="26d8a-122">-DatasetGranularity</span></span>
<span data-ttu-id="26d8a-123">A lekérdezés sorai részletessége.</span><span class="sxs-lookup"><span data-stu-id="26d8a-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="26d8a-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="26d8a-124">-DatasetGrouping</span></span>
<span data-ttu-id="26d8a-125">Kifejezés szerint csoportosított tömb, amelyet a lekérdezésben használhat.</span><span class="sxs-lookup"><span data-stu-id="26d8a-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="26d8a-126">Ennek létrehozásáról a DATASETGROUPING tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="26d8a-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d8a-127">-DefaultProfile</span></span>
<span data-ttu-id="26d8a-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26d8a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26d8a-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="26d8a-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="26d8a-130">Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="26d8a-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="26d8a-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="26d8a-132">A külső felhőszolgáltató dimenzióval/lekérdezési művelettel társított típusa.</span><span class="sxs-lookup"><span data-stu-id="26d8a-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="26d8a-133">-Scope</span></span>
<span data-ttu-id="26d8a-134">Ide tartozik az "előfizetések/{subscriptionId}/" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}" a számlázási fiók hatóköréhez, a "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' a invoiceSection hatóköréhez, valamint a "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}" partnerspecifikus.</span><span class="sxs-lookup"><span data-stu-id="26d8a-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-135">-Timeframe</span><span class="sxs-lookup"><span data-stu-id="26d8a-135">-Timeframe</span></span>
<span data-ttu-id="26d8a-136">A lekérdezés adatainak behúzására vonatkozó időkeret.</span><span class="sxs-lookup"><span data-stu-id="26d8a-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="26d8a-137">-TimePeriodFrom</span></span>
<span data-ttu-id="26d8a-138">A kezdő dátum, amelyből az adatokat ki kell húzni.</span><span class="sxs-lookup"><span data-stu-id="26d8a-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="26d8a-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="26d8a-139">-TimePeriodTo</span></span>
<span data-ttu-id="26d8a-140">A záró dátum, amelybe az adatokat le kell húzni.</span><span class="sxs-lookup"><span data-stu-id="26d8a-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="26d8a-141">-Type</span><span class="sxs-lookup"><span data-stu-id="26d8a-141">-Type</span></span>
<span data-ttu-id="26d8a-142">A lekérdezés típusa.</span><span class="sxs-lookup"><span data-stu-id="26d8a-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8a-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26d8a-143">-Confirm</span></span>
<span data-ttu-id="26d8a-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26d8a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d8a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d8a-145">-WhatIf</span></span>
<span data-ttu-id="26d8a-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26d8a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26d8a-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26d8a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d8a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d8a-148">CommonParameters</span></span>
<span data-ttu-id="26d8a-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26d8a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d8a-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26d8a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d8a-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26d8a-151">INPUTS</span></span>

## <span data-ttu-id="26d8a-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26d8a-152">OUTPUTS</span></span>

### <span data-ttu-id="26d8a-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="26d8a-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="26d8a-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26d8a-154">NOTES</span></span>

<span data-ttu-id="26d8a-155">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="26d8a-155">ALIASES</span></span>

<span data-ttu-id="26d8a-156">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="26d8a-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26d8a-157">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="26d8a-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26d8a-158">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26d8a-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26d8a-159">DATASETFILTER: A lekérdezésben használható <IQueryFilter> szűrőkifejezéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="26d8a-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="26d8a-160">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="26d8a-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="26d8a-161">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="26d8a-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="26d8a-162">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="26d8a-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="26d8a-163">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="26d8a-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="26d8a-164">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="26d8a-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="26d8a-165">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="26d8a-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="26d8a-166">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="26d8a-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="26d8a-167">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="26d8a-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="26d8a-168">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="26d8a-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="26d8a-169">DATASETGROUPING <IQueryGrouping[]>: A lekérdezésben használható csoportkifejezések tömbje.</span><span class="sxs-lookup"><span data-stu-id="26d8a-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="26d8a-170">`Name <String>`: A csoportosított oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="26d8a-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="26d8a-171">`Type <QueryColumnType>`: Csoportosított oszloptípussal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="26d8a-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="26d8a-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26d8a-172">RELATED LINKS</span></span>

