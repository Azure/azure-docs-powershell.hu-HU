---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924065"
---
# <span data-ttu-id="5d92a-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5d92a-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="5d92a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d92a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d92a-103">Létrehoz egy helyi dimenziókijelölési objektumot, amely metrikus riasztási feltételek kiszámítására használható.</span><span class="sxs-lookup"><span data-stu-id="5d92a-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="5d92a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d92a-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d92a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d92a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d92a-106">A **New-AzMetricAlertRuleV2DimensionSelection parancsmag** helyi dimenziókiválasztási objektumot hoz létre, amely segít a metrikus riasztási feltételek [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) parancsmaggal való megépítésében.</span><span class="sxs-lookup"><span data-stu-id="5d92a-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="5d92a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d92a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d92a-108">1. példa: Méretezéskijelölési objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="5d92a-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="5d92a-109">Ez a parancs létrehoz egy méretezéskijelölési objektumot, amely megadja, hogy az értékeket ki kell választani {1,3,4} a Dimenzió "LUN" beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="5d92a-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="5d92a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d92a-110">PARAMETERS</span></span>

### <span data-ttu-id="5d92a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d92a-111">-DefaultProfile</span></span>
<span data-ttu-id="5d92a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d92a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d92a-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="5d92a-113">-DimensionName</span></span>
<span data-ttu-id="5d92a-114">A dimenzió neve</span><span class="sxs-lookup"><span data-stu-id="5d92a-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d92a-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="5d92a-115">-ValuesToExclude</span></span>
<span data-ttu-id="5d92a-116">The ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="5d92a-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d92a-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="5d92a-117">-ValuesToInclude</span></span>
<span data-ttu-id="5d92a-118">Az IncludeValues</span><span class="sxs-lookup"><span data-stu-id="5d92a-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d92a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d92a-119">CommonParameters</span></span>
<span data-ttu-id="5d92a-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d92a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d92a-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d92a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d92a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d92a-122">INPUTS</span></span>

### <span data-ttu-id="5d92a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5d92a-123">System.String</span></span>

### <span data-ttu-id="5d92a-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5d92a-124">System.String[]</span></span>

## <span data-ttu-id="5d92a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d92a-125">OUTPUTS</span></span>

### <span data-ttu-id="5d92a-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="5d92a-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="5d92a-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d92a-127">NOTES</span></span>

## <span data-ttu-id="5d92a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d92a-128">RELATED LINKS</span></span>
