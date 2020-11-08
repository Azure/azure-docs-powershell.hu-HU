---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011988"
---
# <span data-ttu-id="91e68-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="91e68-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="91e68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91e68-102">SYNOPSIS</span></span>
<span data-ttu-id="91e68-103">Engedélyezi az Azure Advisor-ajánlás (oka) t.</span><span class="sxs-lookup"><span data-stu-id="91e68-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="91e68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91e68-104">SYNTAX</span></span>

### <span data-ttu-id="91e68-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91e68-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e68-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e68-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e68-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e68-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e68-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91e68-108">DESCRIPTION</span></span>
<span data-ttu-id="91e68-109">Ez a parancsmag lehetővé teszi a korábban elnyomott ajánlást.</span><span class="sxs-lookup"><span data-stu-id="91e68-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="91e68-110">Eltávolíthatja az ajánlással társított összes eltávolítást is.</span><span class="sxs-lookup"><span data-stu-id="91e68-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="91e68-111">Példák</span><span class="sxs-lookup"><span data-stu-id="91e68-111">EXAMPLES</span></span>

### <span data-ttu-id="91e68-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91e68-112">Example 1</span></span>
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

<span data-ttu-id="91e68-113">A "recommendation_id" néven megadott ajánlás összes eltávolítását eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="91e68-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="91e68-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="91e68-114">Example 2</span></span>
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

<span data-ttu-id="91e68-115">Eltávolítja a csővezetékről átadott ajánlás (ok) összes eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="91e68-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="91e68-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91e68-116">PARAMETERS</span></span>

### <span data-ttu-id="91e68-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91e68-117">-Confirm</span></span>
<span data-ttu-id="91e68-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91e68-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e68-119">-DefaultProfile</span></span>
<span data-ttu-id="91e68-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91e68-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91e68-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91e68-121">-InputObject</span></span>
<span data-ttu-id="91e68-122">Get-AzAdvisorRecommendation hívás által visszaadott PowerShell-objektum típusa: PsAzureAdvisorResourceRecommendationBase.</span><span class="sxs-lookup"><span data-stu-id="91e68-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="91e68-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="91e68-123">-RecommendationName</span></span>
<span data-ttu-id="91e68-124">ResourceName az ajánlást.</span><span class="sxs-lookup"><span data-stu-id="91e68-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="91e68-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91e68-125">-ResourceId</span></span>
<span data-ttu-id="91e68-126">Annak az ajánlásnak az azonosítója, amelyet el kell tiltani.</span><span class="sxs-lookup"><span data-stu-id="91e68-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="91e68-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e68-127">-WhatIf</span></span>
<span data-ttu-id="91e68-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91e68-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91e68-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91e68-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e68-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e68-130">CommonParameters</span></span>
<span data-ttu-id="91e68-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91e68-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="91e68-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e68-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e68-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91e68-133">INPUTS</span></span>

### <span data-ttu-id="91e68-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91e68-134">System.String</span></span>

### <span data-ttu-id="91e68-135">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="91e68-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="91e68-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91e68-136">OUTPUTS</span></span>

### <span data-ttu-id="91e68-137">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="91e68-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="91e68-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91e68-138">NOTES</span></span>

## <span data-ttu-id="91e68-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91e68-139">RELATED LINKS</span></span>
