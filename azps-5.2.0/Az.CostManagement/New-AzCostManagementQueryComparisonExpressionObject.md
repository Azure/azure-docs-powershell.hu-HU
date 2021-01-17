---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336641"
---
# <span data-ttu-id="08cda-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="08cda-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="08cda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08cda-102">SYNOPSIS</span></span>
<span data-ttu-id="08cda-103">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="08cda-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="08cda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08cda-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="08cda-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08cda-105">DESCRIPTION</span></span>
<span data-ttu-id="08cda-106">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="08cda-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="08cda-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08cda-107">EXAMPLES</span></span>

### <span data-ttu-id="08cda-108">1. példa: Összehasonlítási kifejezésobjektum létrehozása a költségkezelési exportáláshoz</span><span class="sxs-lookup"><span data-stu-id="08cda-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="08cda-109">Ez a parancs egy összehasonlító kifejezésobjektumot hoz létre a költségkezelési exportáláshoz.</span><span class="sxs-lookup"><span data-stu-id="08cda-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="08cda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08cda-110">PARAMETERS</span></span>

### <span data-ttu-id="08cda-111">-Name</span><span class="sxs-lookup"><span data-stu-id="08cda-111">-Name</span></span>
<span data-ttu-id="08cda-112">Az összehasonlításban használt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="08cda-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="08cda-113">-Operátor</span><span class="sxs-lookup"><span data-stu-id="08cda-113">-Operator</span></span>
<span data-ttu-id="08cda-114">Az összehasonlításhoz használt operátor.</span><span class="sxs-lookup"><span data-stu-id="08cda-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="08cda-115">-Érték</span><span class="sxs-lookup"><span data-stu-id="08cda-115">-Value</span></span>
<span data-ttu-id="08cda-116">Az összehasonlításhoz használható értékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="08cda-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="08cda-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cda-117">CommonParameters</span></span>
<span data-ttu-id="08cda-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08cda-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cda-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08cda-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cda-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08cda-120">INPUTS</span></span>

## <span data-ttu-id="08cda-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08cda-121">OUTPUTS</span></span>

### <span data-ttu-id="08cda-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="08cda-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="08cda-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08cda-123">NOTES</span></span>

<span data-ttu-id="08cda-124">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="08cda-124">ALIASES</span></span>

## <span data-ttu-id="08cda-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08cda-125">RELATED LINKS</span></span>

