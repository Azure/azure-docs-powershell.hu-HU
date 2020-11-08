---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010532"
---
# <span data-ttu-id="7cf52-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="7cf52-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="7cf52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cf52-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf52-103">Az adattó-elemzés frissíti egy adott AAD-entitásra vonatkozó házirend-szabályt.</span><span class="sxs-lookup"><span data-stu-id="7cf52-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="7cf52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cf52-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cf52-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf52-106">Az **Update-AzDataLakeAnalyticsComputePolicy** frissíti az Azure Data Lake-beli Analytics-fiókban meghatározott aad-entitásokra vonatkozó meghatározott számítási házirend-szabályt.</span><span class="sxs-lookup"><span data-stu-id="7cf52-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7cf52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7cf52-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf52-108">Példa 1: egy szabály frissítése egy számítási házirendben</span><span class="sxs-lookup"><span data-stu-id="7cf52-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="7cf52-109">Ez a parancs frissíti a "contosoadla" fiók "myPolicy" nevű házirendjét, így biztosítva, hogy a felhasználó semmilyen munkát ne nyújtson be több mint 5 elemzési egységben.</span><span class="sxs-lookup"><span data-stu-id="7cf52-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="7cf52-110">2. példa: számítási házirend létrehozása a szabályok frissítésével</span><span class="sxs-lookup"><span data-stu-id="7cf52-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="7cf52-111">Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban, hogy a felhasználók nem tudnak több mint 5 Analytics-egységgel vagy a 100-nál kisebb prioritással eljuttatni a feladatot.</span><span class="sxs-lookup"><span data-stu-id="7cf52-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="7cf52-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cf52-112">PARAMETERS</span></span>

### <span data-ttu-id="7cf52-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="7cf52-113">-Account</span></span>
<span data-ttu-id="7cf52-114">Annak a fióknak a neve, amely frissíti a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="7cf52-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="7cf52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf52-115">-DefaultProfile</span></span>
<span data-ttu-id="7cf52-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7cf52-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cf52-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="7cf52-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="7cf52-118">A házirendben a maximálisan támogatott elemzési egységek száma.</span><span class="sxs-lookup"><span data-stu-id="7cf52-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="7cf52-119">Ezt, MinPriorityPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="7cf52-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="7cf52-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="7cf52-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="7cf52-121">A házirendre vonatkozó, a minimálisan támogatott prioritás.</span><span class="sxs-lookup"><span data-stu-id="7cf52-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="7cf52-122">Ezt, MaxAnalyticsUnitsPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="7cf52-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="7cf52-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cf52-123">-Name</span></span>
<span data-ttu-id="7cf52-124">Annak a számítási házirendnek a neve, amelyet frissíteni szeretne.</span><span class="sxs-lookup"><span data-stu-id="7cf52-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="7cf52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf52-125">-ResourceGroupName</span></span>
<span data-ttu-id="7cf52-126">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="7cf52-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="7cf52-127">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="7cf52-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="7cf52-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cf52-128">-Confirm</span></span>
<span data-ttu-id="7cf52-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cf52-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf52-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf52-130">-WhatIf</span></span>
<span data-ttu-id="7cf52-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cf52-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cf52-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cf52-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf52-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf52-133">CommonParameters</span></span>
<span data-ttu-id="7cf52-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cf52-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf52-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf52-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf52-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf52-136">INPUTS</span></span>

### <span data-ttu-id="7cf52-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf52-137">System.String</span></span>

### <span data-ttu-id="7cf52-138">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7cf52-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7cf52-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf52-139">OUTPUTS</span></span>

### <span data-ttu-id="7cf52-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="7cf52-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="7cf52-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cf52-141">NOTES</span></span>

## <span data-ttu-id="7cf52-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cf52-142">RELATED LINKS</span></span>
