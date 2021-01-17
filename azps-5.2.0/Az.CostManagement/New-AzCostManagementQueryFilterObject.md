---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336617"
---
# <span data-ttu-id="2a964-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="2a964-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="2a964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a964-102">SYNOPSIS</span></span>
<span data-ttu-id="2a964-103">Memória-objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="2a964-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="2a964-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a964-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="2a964-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a964-105">DESCRIPTION</span></span>
<span data-ttu-id="2a964-106">Memória-objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="2a964-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="2a964-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a964-107">EXAMPLES</span></span>

### <span data-ttu-id="2a964-108">1. példa: Lekérdezés szűrőobjektumának létrehozása költségkezelési exportáláshoz</span><span class="sxs-lookup"><span data-stu-id="2a964-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="2a964-109">ez a parancs egy lekérdezésszűrő objektumot hoz létre a költségkezelési exportáláshoz.</span><span class="sxs-lookup"><span data-stu-id="2a964-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="2a964-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a964-110">PARAMETERS</span></span>

### <span data-ttu-id="2a964-111">-And</span><span class="sxs-lookup"><span data-stu-id="2a964-111">-And</span></span>
<span data-ttu-id="2a964-112">A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-112">The logical "AND" expression.</span></span>
<span data-ttu-id="2a964-113">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-113">Must have at least 2 items.</span></span>
<span data-ttu-id="2a964-114">Ennek létrehozásáról az AND tulajdonságokat és a kivonattáblát a JEGYZETEK szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="2a964-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a964-115">-Méretek</span><span class="sxs-lookup"><span data-stu-id="2a964-115">-Dimensions</span></span>
<span data-ttu-id="2a964-116">A dimenziók összehasonlító kifejezéssel vannak meg kifejezve.</span><span class="sxs-lookup"><span data-stu-id="2a964-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="2a964-117">Ennek létrehozásához a NOTES (JEGYZETEK) szakaszban láthatja a DIMENSIONS tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="2a964-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a964-118">-Not</span><span class="sxs-lookup"><span data-stu-id="2a964-118">-Not</span></span>
<span data-ttu-id="2a964-119">A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="2a964-120">A NEM tulajdonságok létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="2a964-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a964-121">-Vagy</span><span class="sxs-lookup"><span data-stu-id="2a964-121">-Or</span></span>
<span data-ttu-id="2a964-122">A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-122">The logical "OR" expression.</span></span>
<span data-ttu-id="2a964-123">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-123">Must have at least 2 items.</span></span>
<span data-ttu-id="2a964-124">Ennek létrehozásáról a VAGY tulajdonságokat a NOTES (VAGY) című szakaszban, valamint egy kivonattáblát hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="2a964-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a964-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a964-125">-Tag</span></span>
<span data-ttu-id="2a964-126">Egy címkéhez összehasonlító kifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a964-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="2a964-127">A címkék tulajdonságainak létrehozásáról és a kivonattáblák létrehozásáról a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="2a964-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a964-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a964-128">CommonParameters</span></span>
<span data-ttu-id="2a964-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a964-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a964-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a964-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a964-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a964-131">INPUTS</span></span>

## <span data-ttu-id="2a964-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a964-132">OUTPUTS</span></span>

### <span data-ttu-id="2a964-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="2a964-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="2a964-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a964-134">NOTES</span></span>

<span data-ttu-id="2a964-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2a964-135">ALIASES</span></span>

<span data-ttu-id="2a964-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2a964-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a964-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2a964-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a964-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a964-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a964-139">ÉS <IQueryFilter[]>: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="2a964-140">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-141">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="2a964-142">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-143">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="2a964-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="2a964-144">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="2a964-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="2a964-145">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="2a964-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="2a964-146">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="2a964-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="2a964-147">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a964-148">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="2a964-149">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-150">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="2a964-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="2a964-151"><IQueryComparisonExpression>MÉRETEK: Dimenziók összehasonlító kifejezését tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2a964-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="2a964-152">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="2a964-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="2a964-153">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="2a964-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="2a964-154">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="2a964-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="2a964-155">NOT <IQueryFilter> : A logikai "NOT" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a964-156">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="2a964-157">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-158">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="2a964-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="2a964-159">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="2a964-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="2a964-160">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="2a964-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="2a964-161">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="2a964-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="2a964-162">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a964-163">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="2a964-164">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-165">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="2a964-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="2a964-166">OR <IQueryFilter[]>: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="2a964-167">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-168">`[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="2a964-169">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-170">`[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="2a964-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="2a964-171">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="2a964-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="2a964-172">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="2a964-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="2a964-173">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="2a964-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="2a964-174">`[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a964-175">`[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés.</span><span class="sxs-lookup"><span data-stu-id="2a964-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="2a964-176">Legalább 2 elemet kell tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2a964-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a964-177">`[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad</span><span class="sxs-lookup"><span data-stu-id="2a964-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="2a964-178">CÍMKE: <IQueryComparisonExpression> Egy címkéhez összehasonlító kifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a964-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="2a964-179">`Name <String>`: Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="2a964-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="2a964-180">`Operator <OperatorType>`: Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="2a964-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="2a964-181">`Value <String[]>`: Az összehasonlításhoz használható értékek tömbje</span><span class="sxs-lookup"><span data-stu-id="2a964-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="2a964-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a964-182">RELATED LINKS</span></span>

