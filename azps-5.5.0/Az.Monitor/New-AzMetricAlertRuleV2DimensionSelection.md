---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157354"
---
# <span data-ttu-id="a6045-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a6045-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="a6045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6045-102">SYNOPSIS</span></span>
<span data-ttu-id="a6045-103">Létrehoz egy helyi dimenziókijelölési objektumot, amely metrikus riasztási feltételek kiszámítására használható.</span><span class="sxs-lookup"><span data-stu-id="a6045-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="a6045-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6045-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6045-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6045-105">DESCRIPTION</span></span>
<span data-ttu-id="a6045-106">A **New-AzMetricAlertRuleV2DimensionSelection parancsmag** létrehoz egy helyi dimenziókiválasztási objektumot, amely segít a metrikus riasztási feltételek [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) parancsmag használatával való megépítésében.</span><span class="sxs-lookup"><span data-stu-id="a6045-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="a6045-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6045-107">EXAMPLES</span></span>

### <span data-ttu-id="a6045-108">1. példa: Méretezéskijelölési objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a6045-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="a6045-109">Ez a parancs létrehoz egy méretezéskijelölési objektumot, amely megadja, hogy az értékeket ki kell választani {1,3,4} a Dimenzió "LUN" beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="a6045-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="a6045-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6045-110">PARAMETERS</span></span>

### <span data-ttu-id="a6045-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6045-111">-DefaultProfile</span></span>
<span data-ttu-id="a6045-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6045-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6045-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="a6045-113">-DimensionName</span></span>
<span data-ttu-id="a6045-114">A dimenzió neve</span><span class="sxs-lookup"><span data-stu-id="a6045-114">The Dimension name</span></span>

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

### <span data-ttu-id="a6045-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="a6045-115">-ValuesToExclude</span></span>
<span data-ttu-id="a6045-116">The ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="a6045-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="a6045-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="a6045-117">-ValuesToInclude</span></span>
<span data-ttu-id="a6045-118">Az IncludeValues</span><span class="sxs-lookup"><span data-stu-id="a6045-118">The IncludeValues</span></span>

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

### <span data-ttu-id="a6045-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6045-119">CommonParameters</span></span>
<span data-ttu-id="a6045-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6045-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6045-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6045-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6045-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6045-122">INPUTS</span></span>

### <span data-ttu-id="a6045-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a6045-123">System.String</span></span>

### <span data-ttu-id="a6045-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a6045-124">System.String[]</span></span>

## <span data-ttu-id="a6045-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6045-125">OUTPUTS</span></span>

### <span data-ttu-id="a6045-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="a6045-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="a6045-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6045-127">NOTES</span></span>

## <span data-ttu-id="a6045-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6045-128">RELATED LINKS</span></span>
