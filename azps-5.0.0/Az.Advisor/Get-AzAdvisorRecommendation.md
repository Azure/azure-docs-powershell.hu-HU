---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303908"
---
# <span data-ttu-id="31a43-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="31a43-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="31a43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31a43-102">SYNOPSIS</span></span>
<span data-ttu-id="31a43-103">Az Azure Advisor-javaslatok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="31a43-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="31a43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31a43-104">SYNTAX</span></span>

### <span data-ttu-id="31a43-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31a43-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31a43-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31a43-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31a43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="31a43-107">DESCRIPTION</span></span>
<span data-ttu-id="31a43-108">Beolvassa az Azure Advisor-javaslatok listáját.</span><span class="sxs-lookup"><span data-stu-id="31a43-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="31a43-109">Lehet szűrni kategória, erőforrás-azonosító, név stb.</span><span class="sxs-lookup"><span data-stu-id="31a43-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="31a43-110">Példák</span><span class="sxs-lookup"><span data-stu-id="31a43-110">EXAMPLES</span></span>

### <span data-ttu-id="31a43-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="31a43-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="31a43-112">Megkapja az összes javaslat listáját.</span><span class="sxs-lookup"><span data-stu-id="31a43-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="31a43-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="31a43-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="31a43-114">A kategória szerinti teljesítménnyel szűrt javaslatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31a43-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="31a43-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31a43-115">PARAMETERS</span></span>

### <span data-ttu-id="31a43-116">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="31a43-116">-Category</span></span>
<span data-ttu-id="31a43-117">Az ajánlás kategóriája</span><span class="sxs-lookup"><span data-stu-id="31a43-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a43-118">-DefaultProfile</span></span>
<span data-ttu-id="31a43-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31a43-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a43-120">-ResourceGroupName</span></span>
<span data-ttu-id="31a43-121">Az ajánlás ResourceGroup neve</span><span class="sxs-lookup"><span data-stu-id="31a43-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a43-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31a43-122">-ResourceId</span></span>
<span data-ttu-id="31a43-123">Az ajánlás ResourceId</span><span class="sxs-lookup"><span data-stu-id="31a43-123">ResourceId of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a43-124">CommonParameters</span></span>
<span data-ttu-id="31a43-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31a43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="31a43-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a43-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a43-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a43-127">INPUTS</span></span>

### <span data-ttu-id="31a43-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31a43-128">System.String</span></span>

## <span data-ttu-id="31a43-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a43-129">OUTPUTS</span></span>

### <span data-ttu-id="31a43-130">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="31a43-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="31a43-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31a43-131">NOTES</span></span>

## <span data-ttu-id="31a43-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31a43-132">RELATED LINKS</span></span>
