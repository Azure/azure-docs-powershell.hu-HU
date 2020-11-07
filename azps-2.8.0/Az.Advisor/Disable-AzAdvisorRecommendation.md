---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668219"
---
# <span data-ttu-id="e562e-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="e562e-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="e562e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e562e-102">SYNOPSIS</span></span>
<span data-ttu-id="e562e-103">Tiltsa le az Azure Advisor-ajánlást.</span><span class="sxs-lookup"><span data-stu-id="e562e-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="e562e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e562e-104">SYNTAX</span></span>

### <span data-ttu-id="e562e-105">IdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e562e-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e562e-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e562e-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e562e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e562e-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e562e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e562e-108">DESCRIPTION</span></span>
<span data-ttu-id="e562e-109">Elfojtást hoz létre az ajánlás (ok) számára, amely lehetővé teszi, hogy egy adott ajánlás meghatározott időtartamra vagy végtelenre elhalasztható legyen.</span><span class="sxs-lookup"><span data-stu-id="e562e-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="e562e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e562e-110">EXAMPLES</span></span>

### <span data-ttu-id="e562e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e562e-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="e562e-112">Elfojtást hozhat létre a megadott ajánlás nevében alapértelmezett-SuppressionName és alapértelmezett napok szerint-1 értékkel.</span><span class="sxs-lookup"><span data-stu-id="e562e-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="e562e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e562e-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="e562e-114">A program az adott ajánlás-azonosítóhoz hoz létre adateltávolítást.</span><span class="sxs-lookup"><span data-stu-id="e562e-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="e562e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e562e-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="e562e-116">Elfojtást, csöveket Get-AzAdvisorRecommendationból letiltani – AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="e562e-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="e562e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e562e-117">PARAMETERS</span></span>

### <span data-ttu-id="e562e-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e562e-118">-Confirm</span></span>
<span data-ttu-id="e562e-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e562e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e562e-120">-Days</span><span class="sxs-lookup"><span data-stu-id="e562e-120">-Days</span></span>
<span data-ttu-id="e562e-121">Letiltani kívánt napok</span><span class="sxs-lookup"><span data-stu-id="e562e-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e562e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e562e-122">-DefaultProfile</span></span>
<span data-ttu-id="e562e-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e562e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e562e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e562e-124">-InputObject</span></span>
<span data-ttu-id="e562e-125">Get-AzAdvisorRecommendation hívás által visszaadott PowerShell-objektum típusa: PsAzureAdvisorResourceRecommendationBase.</span><span class="sxs-lookup"><span data-stu-id="e562e-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="e562e-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="e562e-126">-RecommendationName</span></span>
<span data-ttu-id="e562e-127">Az ajánlás ResourceName</span><span class="sxs-lookup"><span data-stu-id="e562e-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="e562e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e562e-128">-ResourceId</span></span>
<span data-ttu-id="e562e-129">Annak az ajánlásnak az azonosítója, amelyet el kell tiltani.</span><span class="sxs-lookup"><span data-stu-id="e562e-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e562e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e562e-130">-WhatIf</span></span>
<span data-ttu-id="e562e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e562e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e562e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e562e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e562e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e562e-133">CommonParameters</span></span>
<span data-ttu-id="e562e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e562e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e562e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e562e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e562e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e562e-136">INPUTS</span></span>

### <span data-ttu-id="e562e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e562e-137">System.String</span></span>

### <span data-ttu-id="e562e-138">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="e562e-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="e562e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e562e-139">OUTPUTS</span></span>

### <span data-ttu-id="e562e-140">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="e562e-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="e562e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e562e-141">NOTES</span></span>

## <span data-ttu-id="e562e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e562e-142">RELATED LINKS</span></span>
