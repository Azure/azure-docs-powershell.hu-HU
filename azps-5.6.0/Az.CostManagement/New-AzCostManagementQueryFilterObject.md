---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010646"
---
# <span data-ttu-id="9dda4-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="9dda4-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="9dda4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dda4-102">SYNOPSIS</span></span>
<span data-ttu-id="9dda4-103">Memória-objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="9dda4-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="9dda4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9dda4-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="9dda4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9dda4-105">DESCRIPTION</span></span>
<span data-ttu-id="9dda4-106">Memória-objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="9dda4-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="9dda4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9dda4-107">EXAMPLES</span></span>

### <span data-ttu-id="9dda4-108">1. példa: Lekérdezés szűrőobjektumának létrehozása költségkezelési exportáláshoz</span><span class="sxs-lookup"><span data-stu-id="9dda4-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="9dda4-109">ez a parancs egy lekérdezésszűrő objektumot hoz létre a költségkezelési exportáláshoz.</span><span class="sxs-lookup"><span data-stu-id="9dda4-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="9dda4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dda4-110">PARAMETERS</span></span>

### <span data-ttu-id="9dda4-111">-And</span><span class="sxs-lookup"><span data-stu-id="9dda4-111">-And</span></span>
<span data-ttu-id="9dda4-112">A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-112">The logical "AND" expression.</span></span>
<span data-ttu-id="9dda4-113">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-113">Must have at least 2 items.</span></span>
<span data-ttu-id="9dda4-114">Ennek létrehozásáról az AND tulajdonságokat és a kivonattáblát a JEGYZETEK szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="9dda4-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="9dda4-115">-Méretek</span><span class="sxs-lookup"><span data-stu-id="9dda4-115">-Dimensions</span></span>
<span data-ttu-id="9dda4-116">A dimenziók összehasonlító kifejezéssel vannak meg kifejezve.</span><span class="sxs-lookup"><span data-stu-id="9dda4-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="9dda4-117">Ennek létrehozásához a NOTES (JEGYZETEK) szakaszban láthatja a DIMENSIONS tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="9dda4-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="9dda4-118">-Not</span><span class="sxs-lookup"><span data-stu-id="9dda4-118">-Not</span></span>
<span data-ttu-id="9dda4-119">A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="9dda4-120">A NEM tulajdonságok létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="9dda4-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9dda4-121">-Vagy</span><span class="sxs-lookup"><span data-stu-id="9dda4-121">-Or</span></span>
<span data-ttu-id="9dda4-122">A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-122">The logical "OR" expression.</span></span>
<span data-ttu-id="9dda4-123">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-123">Must have at least 2 items.</span></span>
<span data-ttu-id="9dda4-124">Ennek létrehozásáról a VAGY tulajdonságokat a NOTES (VAGY) című szakaszban, valamint egy kivonattáblát hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="9dda4-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="9dda4-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dda4-125">-Tag</span></span>
<span data-ttu-id="9dda4-126">Egy címkéhez összehasonlító kifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="9dda4-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="9dda4-127">A címkék tulajdonságainak létrehozásáról és a kivonattáblák létrehozásáról a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="9dda4-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="9dda4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dda4-128">CommonParameters</span></span>
<span data-ttu-id="9dda4-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dda4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dda4-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dda4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dda4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dda4-131">INPUTS</span></span>

## <span data-ttu-id="9dda4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dda4-132">OUTPUTS</span></span>

### <span data-ttu-id="9dda4-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="9dda4-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="9dda4-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9dda4-134">NOTES</span></span>

<span data-ttu-id="9dda4-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9dda4-135">ALIASES</span></span>

<span data-ttu-id="9dda4-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9dda4-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9dda4-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9dda4-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9dda4-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9dda4-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9dda4-139">ÉS <IQueryFilter[]>: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="9dda4-140">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-141">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="9dda4-142">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-143">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="9dda4-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="9dda4-144">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9dda4-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="9dda4-145">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="9dda4-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="9dda4-146">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9dda4-147">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="9dda4-148">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-149">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="9dda4-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="9dda4-150"><IQueryComparisonExpression>MÉRETEK: Dimenziók összehasonlító kifejezését tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9dda4-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="9dda4-151">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9dda4-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="9dda4-152">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="9dda4-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="9dda4-153">NOT <IQueryFilter> : A logikai "NOT" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9dda4-154">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="9dda4-155">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-156">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="9dda4-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="9dda4-157">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9dda4-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="9dda4-158">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="9dda4-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="9dda4-159">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9dda4-160">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="9dda4-161">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-162">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="9dda4-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="9dda4-163">OR <IQueryFilter[]>: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="9dda4-164">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-165">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="9dda4-166">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-167">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="9dda4-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="9dda4-168">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9dda4-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="9dda4-169">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="9dda4-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="9dda4-170">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9dda4-171">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="9dda4-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="9dda4-172">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9dda4-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9dda4-173">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="9dda4-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="9dda4-174">CÍMKE: <IQueryComparisonExpression> Egy címkéhez összehasonlító kifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="9dda4-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="9dda4-175">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9dda4-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="9dda4-176">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="9dda4-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="9dda4-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dda4-177">RELATED LINKS</span></span>

