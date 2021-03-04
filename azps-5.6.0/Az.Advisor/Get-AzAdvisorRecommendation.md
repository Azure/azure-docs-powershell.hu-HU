---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 9d45db213cf3569837c6b35284c95dc9a076a381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926114"
---
# <span data-ttu-id="77ea4-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="77ea4-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="77ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="77ea4-103">Az Azure Advisor javaslatainak listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="77ea4-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="77ea4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77ea4-104">SYNTAX</span></span>

### <span data-ttu-id="77ea4-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77ea4-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77ea4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77ea4-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77ea4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77ea4-107">DESCRIPTION</span></span>
<span data-ttu-id="77ea4-108">Lekérte az Azure Advisor-javaslatok listáját.</span><span class="sxs-lookup"><span data-stu-id="77ea4-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="77ea4-109">Kategória, erőforrás-azonosító, név stb. szerint szűrhető.</span><span class="sxs-lookup"><span data-stu-id="77ea4-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="77ea4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77ea4-110">EXAMPLES</span></span>

### <span data-ttu-id="77ea4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="77ea4-111">Example 1</span></span>
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
<span data-ttu-id="77ea4-112">Az összes javaslat listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="77ea4-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="77ea4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="77ea4-113">Example 2</span></span>
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
<span data-ttu-id="77ea4-114">Az összes javaslat listáját kategóriateljesítmény szerint szűri.</span><span class="sxs-lookup"><span data-stu-id="77ea4-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="77ea4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77ea4-115">PARAMETERS</span></span>

### <span data-ttu-id="77ea4-116">-Category</span><span class="sxs-lookup"><span data-stu-id="77ea4-116">-Category</span></span>
<span data-ttu-id="77ea4-117">Az ajánlott kategória</span><span class="sxs-lookup"><span data-stu-id="77ea4-117">Category of the recommendation</span></span>

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

### <span data-ttu-id="77ea4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ea4-118">-DefaultProfile</span></span>
<span data-ttu-id="77ea4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77ea4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ea4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ea4-120">-ResourceGroupName</span></span>
<span data-ttu-id="77ea4-121">A javaslat Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="77ea4-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="77ea4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77ea4-122">-ResourceId</span></span>
<span data-ttu-id="77ea4-123">ResourceId of the recommendation</span><span class="sxs-lookup"><span data-stu-id="77ea4-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="77ea4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ea4-124">CommonParameters</span></span>
<span data-ttu-id="77ea4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ea4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77ea4-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ea4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ea4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77ea4-127">INPUTS</span></span>

### <span data-ttu-id="77ea4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="77ea4-128">System.String</span></span>

## <span data-ttu-id="77ea4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77ea4-129">OUTPUTS</span></span>

### <span data-ttu-id="77ea4-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="77ea4-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="77ea4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77ea4-131">NOTES</span></span>

## <span data-ttu-id="77ea4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77ea4-132">RELATED LINKS</span></span>
