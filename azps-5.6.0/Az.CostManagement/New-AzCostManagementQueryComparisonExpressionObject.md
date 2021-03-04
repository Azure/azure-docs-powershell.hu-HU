---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: b41c5a30a1425778e69fbfff42cfe7062c6b71b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942689"
---
# <span data-ttu-id="83c50-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="83c50-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="83c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83c50-102">SYNOPSIS</span></span>
<span data-ttu-id="83c50-103">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="83c50-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="83c50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83c50-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="83c50-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83c50-105">DESCRIPTION</span></span>
<span data-ttu-id="83c50-106">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="83c50-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="83c50-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83c50-107">EXAMPLES</span></span>

### <span data-ttu-id="83c50-108">1. példa: Összehasonlítási kifejezésobjektum létrehozása a költségkezelési exportáláshoz</span><span class="sxs-lookup"><span data-stu-id="83c50-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="83c50-109">Ez a parancs egy összehasonlító kifejezésobjektumot hoz létre a költségkezelési exportáláshoz.</span><span class="sxs-lookup"><span data-stu-id="83c50-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="83c50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83c50-110">PARAMETERS</span></span>

### <span data-ttu-id="83c50-111">-Name</span><span class="sxs-lookup"><span data-stu-id="83c50-111">-Name</span></span>
<span data-ttu-id="83c50-112">Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="83c50-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="83c50-113">-Operátor</span><span class="sxs-lookup"><span data-stu-id="83c50-113">-Operator</span></span>
<span data-ttu-id="83c50-114">Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="83c50-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="83c50-115">-Érték</span><span class="sxs-lookup"><span data-stu-id="83c50-115">-Value</span></span>
<span data-ttu-id="83c50-116">Az összehasonlításhoz használható értékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="83c50-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="83c50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c50-117">CommonParameters</span></span>
<span data-ttu-id="83c50-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c50-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83c50-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c50-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83c50-120">INPUTS</span></span>

## <span data-ttu-id="83c50-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83c50-121">OUTPUTS</span></span>

### <span data-ttu-id="83c50-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="83c50-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="83c50-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83c50-123">NOTES</span></span>

<span data-ttu-id="83c50-124">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="83c50-124">ALIASES</span></span>

## <span data-ttu-id="83c50-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83c50-125">RELATED LINKS</span></span>

