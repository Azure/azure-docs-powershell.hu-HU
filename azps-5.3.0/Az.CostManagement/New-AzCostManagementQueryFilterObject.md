---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480508"
---
# <span data-ttu-id="0802a-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="0802a-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="0802a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0802a-102">SYNOPSIS</span></span>
<span data-ttu-id="0802a-103">Memóriában létrehozott objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="0802a-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="0802a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0802a-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="0802a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0802a-105">DESCRIPTION</span></span>
<span data-ttu-id="0802a-106">Memóriában létrehozott objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="0802a-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="0802a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0802a-107">EXAMPLES</span></span>

### <span data-ttu-id="0802a-108">1. példa: Lekérdezés szűrőobjektumának létrehozása költségkezelési exportáláshoz</span><span class="sxs-lookup"><span data-stu-id="0802a-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="0802a-109">Ez a parancs egy lekérdezésszűrő objektumot hoz létre a költségkezelési exportáláshoz.</span><span class="sxs-lookup"><span data-stu-id="0802a-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="0802a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0802a-110">PARAMETERS</span></span>

### <span data-ttu-id="0802a-111">-And</span><span class="sxs-lookup"><span data-stu-id="0802a-111">-And</span></span>
<span data-ttu-id="0802a-112">A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-112">The logical "AND" expression.</span></span>
<span data-ttu-id="0802a-113">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-113">Must have at least 2 items.</span></span>
<span data-ttu-id="0802a-114">Ennek létrehozásáról az AND tulajdonságokat és a kivonattáblát a JEGYZETEK szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="0802a-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0802a-115">-Méretek</span><span class="sxs-lookup"><span data-stu-id="0802a-115">-Dimensions</span></span>
<span data-ttu-id="0802a-116">Dimenziókra vonatkozó összehasonlító kifejezéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0802a-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="0802a-117">Ennek létrehozásához a NOTES (JEGYZETEK) szakaszban láthatja a DIMENSIONS tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="0802a-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0802a-118">-Not</span><span class="sxs-lookup"><span data-stu-id="0802a-118">-Not</span></span>
<span data-ttu-id="0802a-119">A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="0802a-120">A NEM tulajdonságok létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="0802a-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0802a-121">-Vagy</span><span class="sxs-lookup"><span data-stu-id="0802a-121">-Or</span></span>
<span data-ttu-id="0802a-122">A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-122">The logical "OR" expression.</span></span>
<span data-ttu-id="0802a-123">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-123">Must have at least 2 items.</span></span>
<span data-ttu-id="0802a-124">Ennek létrehozásáról a VAGY tulajdonságokat a NOTES (VAGY) című szakaszban, valamint egy kivonattáblát hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="0802a-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0802a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="0802a-125">-Tag</span></span>
<span data-ttu-id="0802a-126">Egy címkéhez összehasonlító kifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="0802a-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="0802a-127">A címkék tulajdonságainak létrehozásáról és a kivonattáblák létrehozásáról a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="0802a-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0802a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0802a-128">CommonParameters</span></span>
<span data-ttu-id="0802a-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0802a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0802a-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0802a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0802a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0802a-131">INPUTS</span></span>

## <span data-ttu-id="0802a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0802a-132">OUTPUTS</span></span>

### <span data-ttu-id="0802a-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="0802a-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="0802a-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0802a-134">NOTES</span></span>

<span data-ttu-id="0802a-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0802a-135">ALIASES</span></span>

<span data-ttu-id="0802a-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0802a-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0802a-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0802a-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0802a-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0802a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0802a-139">ÉS <IQueryFilter[]>: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="0802a-140">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-141">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="0802a-142">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-143">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="0802a-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="0802a-144">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="0802a-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="0802a-145">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="0802a-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="0802a-146">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="0802a-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="0802a-147">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="0802a-148">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="0802a-149">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-150">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="0802a-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="0802a-151"><IQueryComparisonExpression>MÉRETEK: Dimenziók összehasonlító kifejezését tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0802a-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="0802a-152">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="0802a-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="0802a-153">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="0802a-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="0802a-154">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="0802a-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="0802a-155">NOT <IQueryFilter> : A logikai "NOT" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="0802a-156">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="0802a-157">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-158">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="0802a-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="0802a-159">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="0802a-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="0802a-160">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="0802a-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="0802a-161">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="0802a-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="0802a-162">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="0802a-163">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="0802a-164">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-165">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="0802a-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="0802a-166">OR <IQueryFilter[]>: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="0802a-167">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-168">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="0802a-169">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-170">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="0802a-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="0802a-171">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="0802a-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="0802a-172">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="0802a-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="0802a-173">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="0802a-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="0802a-174">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="0802a-175">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="0802a-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="0802a-176">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0802a-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0802a-177">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="0802a-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="0802a-178">CÍMKE: <IQueryComparisonExpression> Egy címkéhez összehasonlító kifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="0802a-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="0802a-179">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="0802a-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="0802a-180">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="0802a-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="0802a-181">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="0802a-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="0802a-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0802a-182">RELATED LINKS</span></span>

