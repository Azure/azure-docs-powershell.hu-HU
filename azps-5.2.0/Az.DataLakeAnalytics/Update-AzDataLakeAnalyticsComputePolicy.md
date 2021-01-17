---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372832"
---
# <span data-ttu-id="08c54-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="08c54-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="08c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c54-102">SYNOPSIS</span></span>
<span data-ttu-id="08c54-103">Frissíti a Data Lake Analytics számítási házirendszabályát egy adott AAD-entitáshoz.</span><span class="sxs-lookup"><span data-stu-id="08c54-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="08c54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08c54-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c54-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08c54-105">DESCRIPTION</span></span>
<span data-ttu-id="08c54-106">Az **Update-AzDataLakeAnalyticsComputePolicy** frissíti a megadott számítási házirendszabályt egy Azure Data Lake Analytics-fiók adott AAD-entitásához.</span><span class="sxs-lookup"><span data-stu-id="08c54-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="08c54-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08c54-107">EXAMPLES</span></span>

### <span data-ttu-id="08c54-108">1. példa: Egy szabály frissítése egy számítási házirendben</span><span class="sxs-lookup"><span data-stu-id="08c54-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="08c54-109">Ez a parancs frissíti a "myPolicy" házirendet a "contosoadla" fiókban, hogy a felhasználó ne küldjön be 5-ösnél több elemzési egységben található feladatot.</span><span class="sxs-lookup"><span data-stu-id="08c54-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="08c54-110">2. példa: Számítási házirend létrehozása mindkét szabályfrissítéssel</span><span class="sxs-lookup"><span data-stu-id="08c54-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="08c54-111">Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban, hogy a felhasználó ne küldjön be 5-től több elemzési egységből vagy 100-asnál alacsonyabb prioritású feladatot.</span><span class="sxs-lookup"><span data-stu-id="08c54-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="08c54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08c54-112">PARAMETERS</span></span>

### <span data-ttu-id="08c54-113">-Account</span><span class="sxs-lookup"><span data-stu-id="08c54-113">-Account</span></span>
<span data-ttu-id="08c54-114">Annak a fióknak a neve, amelyben frissíteni szeretné a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="08c54-114">Name of the account to update the compute policy in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c54-115">-DefaultProfile</span></span>
<span data-ttu-id="08c54-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08c54-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08c54-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="08c54-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="08c54-118">A házirendhez a maximális támogatott elemzési egység egy feladathoz.</span><span class="sxs-lookup"><span data-stu-id="08c54-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="08c54-119">Ezt vagy a MinPriorityPerJob paramétert, vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="08c54-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="08c54-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="08c54-121">A házirend minimális támogatott prioritása feladatonként.</span><span class="sxs-lookup"><span data-stu-id="08c54-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="08c54-122">Ezt vagy a MaxAnalyticsUnitsPerJob paramétert, vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="08c54-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-123">-Name</span><span class="sxs-lookup"><span data-stu-id="08c54-123">-Name</span></span>
<span data-ttu-id="08c54-124">A frissítenie kell a számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="08c54-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c54-125">-ResourceGroupName</span></span>
<span data-ttu-id="08c54-126">Annak az erőforráscsoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="08c54-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="08c54-127">Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="08c54-127">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08c54-128">-Confirm</span></span>
<span data-ttu-id="08c54-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="08c54-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c54-130">-WhatIf</span></span>
<span data-ttu-id="08c54-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="08c54-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08c54-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08c54-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c54-133">CommonParameters</span></span>
<span data-ttu-id="08c54-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c54-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c54-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c54-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08c54-136">INPUTS</span></span>

### <span data-ttu-id="08c54-137">System.String</span><span class="sxs-lookup"><span data-stu-id="08c54-137">System.String</span></span>

### <span data-ttu-id="08c54-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08c54-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="08c54-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08c54-139">OUTPUTS</span></span>

### <span data-ttu-id="08c54-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="08c54-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="08c54-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08c54-141">NOTES</span></span>

## <span data-ttu-id="08c54-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08c54-142">RELATED LINKS</span></span>
