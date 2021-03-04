---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 3695ee9d027733d3adea17797ffbcf669136e66b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926138"
---
# <span data-ttu-id="c3869-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="c3869-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="c3869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3869-102">SYNOPSIS</span></span>
<span data-ttu-id="c3869-103">Tiltsa le az Azure Advisor-ajánlást.</span><span class="sxs-lookup"><span data-stu-id="c3869-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="c3869-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3869-104">SYNTAX</span></span>

### <span data-ttu-id="c3869-105">IdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3869-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3869-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3869-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3869-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3869-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3869-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3869-108">DESCRIPTION</span></span>
<span data-ttu-id="c3869-109">Ezzel egy adott javaslat adott időtartamra vagy végtelenül elhalasztható.</span><span class="sxs-lookup"><span data-stu-id="c3869-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="c3869-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3869-110">EXAMPLES</span></span>

### <span data-ttu-id="c3869-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3869-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="c3869-112">Hozzon létre egy 1-es értéket, és hozzon létre egy alapértelmezett 1-es értéket a 1-es értéknek megfelelő 1- és egy alapértelmezett 1-es nevű ajánlott névvel.</span><span class="sxs-lookup"><span data-stu-id="c3869-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="c3869-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3869-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="c3869-114">Egy adott javaslatazonosítóhoz létrejön egy adott javaslatazonosító.</span><span class="sxs-lookup"><span data-stu-id="c3869-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="c3869-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c3869-115">Example 3</span></span>
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

<span data-ttu-id="c3869-116">Ezzel a beállítással a rendszer a Get-AzAdvisorRecommendation Disable-AzAdvisorRecommendation szolgáltatásra irányít.</span><span class="sxs-lookup"><span data-stu-id="c3869-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="c3869-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3869-117">PARAMETERS</span></span>

### <span data-ttu-id="c3869-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3869-118">-Confirm</span></span>
<span data-ttu-id="c3869-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3869-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3869-120">-Days</span><span class="sxs-lookup"><span data-stu-id="c3869-120">-Days</span></span>
<span data-ttu-id="c3869-121">Napok a letiltásig.</span><span class="sxs-lookup"><span data-stu-id="c3869-121">Days to disable.</span></span>

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

### <span data-ttu-id="c3869-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3869-122">-DefaultProfile</span></span>
<span data-ttu-id="c3869-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3869-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3869-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3869-124">-InputObject</span></span>
<span data-ttu-id="c3869-125">A PsAzureAdvisorResourceResourceRecommendationBase powershell-objektumtípus, amelyet egy hívás Get-AzAdvisorRecommendation vissza.</span><span class="sxs-lookup"><span data-stu-id="c3869-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="c3869-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="c3869-126">-RecommendationName</span></span>
<span data-ttu-id="c3869-127">ResourceName of the recommendation</span><span class="sxs-lookup"><span data-stu-id="c3869-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="c3869-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3869-128">-ResourceId</span></span>
<span data-ttu-id="c3869-129">A letiltani fogó javaslat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c3869-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="c3869-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3869-130">-WhatIf</span></span>
<span data-ttu-id="c3869-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3869-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3869-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3869-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3869-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3869-133">CommonParameters</span></span>
<span data-ttu-id="c3869-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3869-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c3869-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3869-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3869-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3869-136">INPUTS</span></span>

### <span data-ttu-id="c3869-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c3869-137">System.String</span></span>

### <span data-ttu-id="c3869-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="c3869-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="c3869-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3869-139">OUTPUTS</span></span>

### <span data-ttu-id="c3869-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="c3869-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="c3869-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3869-141">NOTES</span></span>

## <span data-ttu-id="c3869-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3869-142">RELATED LINKS</span></span>
