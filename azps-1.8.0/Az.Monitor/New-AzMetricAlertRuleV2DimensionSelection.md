---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 349677b4686b2df5a72f233b729a5028dc322057
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835026"
---
# <span data-ttu-id="dfd5e-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="dfd5e-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="dfd5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd5e-103">Létrehoz egy helyi dimenzió kijelölési objektumot, amely metrikus riasztási feltételek kiszámítására használható.</span><span class="sxs-lookup"><span data-stu-id="dfd5e-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="dfd5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfd5e-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfd5e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfd5e-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd5e-106">A **New-AzMetricAlertRuleV2DimensionSelection** parancsmag létrehoz egy helyi dimenzió kijelölési objektumot, amely segítséget nyújt a metrikus riasztási feltételek megépítéséhez a **New-AzMetricAlertRuleV2Criteria** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="dfd5e-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="dfd5e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dfd5e-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd5e-108">Példa 1: méretvonal-választó objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="dfd5e-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}     
```

<span data-ttu-id="dfd5e-109">Ez a parancs létrehoz egy dimenziókészlet-objektumot, amely azt adja meg, hogy {1,3,4} a "LUN" dimenzióhoz milyen értékeket kell kijelölni.</span><span class="sxs-lookup"><span data-stu-id="dfd5e-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="dfd5e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfd5e-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd5e-111">-DefaultProfile</span></span>
<span data-ttu-id="dfd5e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfd5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd5e-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="dfd5e-113">-DimensionName</span></span>
<span data-ttu-id="dfd5e-114">A dimenzió neve</span><span class="sxs-lookup"><span data-stu-id="dfd5e-114">The Dimension name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd5e-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="dfd5e-115">-ValuesToExclude</span></span>
<span data-ttu-id="dfd5e-116">A ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="dfd5e-116">The ExcludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd5e-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="dfd5e-117">-ValuesToInclude</span></span>
<span data-ttu-id="dfd5e-118">A IncludeValues</span><span class="sxs-lookup"><span data-stu-id="dfd5e-118">The IncludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd5e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd5e-119">CommonParameters</span></span>
<span data-ttu-id="dfd5e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfd5e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dfd5e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd5e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd5e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfd5e-122">INPUTS</span></span>

### <span data-ttu-id="dfd5e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dfd5e-123">System.String</span></span>

### <span data-ttu-id="dfd5e-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="dfd5e-124">System.String[]</span></span>

## <span data-ttu-id="dfd5e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfd5e-125">OUTPUTS</span></span>

### <span data-ttu-id="dfd5e-126">Microsoft. Azure. commands. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="dfd5e-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="dfd5e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfd5e-127">NOTES</span></span>

## <span data-ttu-id="dfd5e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfd5e-128">RELATED LINKS</span></span>
