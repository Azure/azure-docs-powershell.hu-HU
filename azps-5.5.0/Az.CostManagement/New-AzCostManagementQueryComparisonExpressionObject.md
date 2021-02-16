---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 608736e8ddb85b877995bed8a42b9bd629dcdba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148403"
---
# <span data-ttu-id="c0b2d-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="c0b2d-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="c0b2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b2d-103">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="c0b2d-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="c0b2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0b2d-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="c0b2d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b2d-106">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="c0b2d-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="c0b2d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0b2d-107">EXAMPLES</span></span>

### <span data-ttu-id="c0b2d-108">1. példa: Összehasonlító kifejezés objektum létrehozása a költségkezelési exportáláshoz</span><span class="sxs-lookup"><span data-stu-id="c0b2d-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="c0b2d-109">Ez a parancs egy összehasonlító kifejezésobjektumot hoz létre a költségkezelési exportáláshoz.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="c0b2d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0b2d-110">PARAMETERS</span></span>

### <span data-ttu-id="c0b2d-111">-Name</span><span class="sxs-lookup"><span data-stu-id="c0b2d-111">-Name</span></span>
<span data-ttu-id="c0b2d-112">Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="c0b2d-113">-Operátor</span><span class="sxs-lookup"><span data-stu-id="c0b2d-113">-Operator</span></span>
<span data-ttu-id="c0b2d-114">Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b2d-115">-Érték</span><span class="sxs-lookup"><span data-stu-id="c0b2d-115">-Value</span></span>
<span data-ttu-id="c0b2d-116">Az összehasonlításhoz használható értékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b2d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b2d-117">CommonParameters</span></span>
<span data-ttu-id="c0b2d-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b2d-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0b2d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b2d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0b2d-120">INPUTS</span></span>

## <span data-ttu-id="c0b2d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0b2d-121">OUTPUTS</span></span>

### <span data-ttu-id="c0b2d-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="c0b2d-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="c0b2d-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0b2d-123">NOTES</span></span>

<span data-ttu-id="c0b2d-124">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c0b2d-124">ALIASES</span></span>

## <span data-ttu-id="c0b2d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0b2d-125">RELATED LINKS</span></span>

