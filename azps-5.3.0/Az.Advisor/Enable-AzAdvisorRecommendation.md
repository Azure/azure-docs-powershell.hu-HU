---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479149"
---
# <span data-ttu-id="1fe21-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="1fe21-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="1fe21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe21-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe21-103">Engedélyezi az Azure Advisor javaslat(ak)t.</span><span class="sxs-lookup"><span data-stu-id="1fe21-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="1fe21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1fe21-104">SYNTAX</span></span>

### <span data-ttu-id="1fe21-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fe21-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe21-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe21-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe21-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe21-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe21-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1fe21-108">DESCRIPTION</span></span>
<span data-ttu-id="1fe21-109">Ez a parancsmag korábban nem használt javaslatot tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="1fe21-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="1fe21-110">Az ajánláshoz társított összes emetkezést is eltávolíthatja.</span><span class="sxs-lookup"><span data-stu-id="1fe21-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="1fe21-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1fe21-111">EXAMPLES</span></span>

### <span data-ttu-id="1fe21-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1fe21-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="1fe21-113">Eltávolítja az adott javaslat összes csökkentését a "recommendation_id" névvel.</span><span class="sxs-lookup"><span data-stu-id="1fe21-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="1fe21-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="1fe21-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="1fe21-115">Eltávolítja a folyamatból a megadott javaslat(ak) összes adatát.</span><span class="sxs-lookup"><span data-stu-id="1fe21-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="1fe21-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fe21-116">PARAMETERS</span></span>

### <span data-ttu-id="1fe21-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fe21-117">-Confirm</span></span>
<span data-ttu-id="1fe21-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1fe21-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe21-119">-DefaultProfile</span></span>
<span data-ttu-id="1fe21-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fe21-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe21-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe21-121">-InputObject</span></span>
<span data-ttu-id="1fe21-122">A PsAzureAdvisorResourceResourceRecommendationBase powershell-objektumtípus, amelyet egy hívás Get-AzAdvisorRecommendation vissza.</span><span class="sxs-lookup"><span data-stu-id="1fe21-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe21-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="1fe21-123">-RecommendationName</span></span>
<span data-ttu-id="1fe21-124">A javaslat Erőforrásneve mezőben.</span><span class="sxs-lookup"><span data-stu-id="1fe21-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe21-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe21-125">-ResourceId</span></span>
<span data-ttu-id="1fe21-126">A letiltani fogó javaslat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1fe21-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="1fe21-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe21-127">-WhatIf</span></span>
<span data-ttu-id="1fe21-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1fe21-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe21-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1fe21-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe21-130">CommonParameters</span></span>
<span data-ttu-id="1fe21-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1fe21-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe21-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe21-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fe21-133">INPUTS</span></span>

### <span data-ttu-id="1fe21-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe21-134">System.String</span></span>

### <span data-ttu-id="1fe21-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="1fe21-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="1fe21-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe21-136">OUTPUTS</span></span>

### <span data-ttu-id="1fe21-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="1fe21-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="1fe21-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1fe21-138">NOTES</span></span>

## <span data-ttu-id="1fe21-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fe21-139">RELATED LINKS</span></span>
