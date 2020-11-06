---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502748"
---
# <span data-ttu-id="3c328-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c328-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c328-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c328-102">SYNOPSIS</span></span>
<span data-ttu-id="3c328-103">Az adattó-elemzés frissíti egy adott AAD-entitásra vonatkozó házirend-szabályt.</span><span class="sxs-lookup"><span data-stu-id="3c328-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c328-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c328-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c328-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c328-105">DESCRIPTION</span></span>
<span data-ttu-id="3c328-106">Az **Update-AzureRmDataLakeAnalyticsComputePolicy** frissíti az Azure Data Lake-beli Analytics-fiókban meghatározott aad-entitásokra vonatkozó meghatározott számítási házirend-szabályt.</span><span class="sxs-lookup"><span data-stu-id="3c328-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3c328-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c328-107">EXAMPLES</span></span>

### <span data-ttu-id="3c328-108">Példa 1: egy szabály frissítése egy számítási házirendben</span><span class="sxs-lookup"><span data-stu-id="3c328-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="3c328-109">Ez a parancs frissíti a "contosoadla" fiók "myPolicy" nevű házirendjét, így biztosítva, hogy a felhasználó nem tud több mint 5 párhuzamosan elküldeni a munkát.</span><span class="sxs-lookup"><span data-stu-id="3c328-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="3c328-110">2. példa: számítási házirend létrehozása a szabályok frissítésével</span><span class="sxs-lookup"><span data-stu-id="3c328-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="3c328-111">Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban, hogy a felhasználó nem tud több mint 5 párhuzamosságtal vagy a 100-nál kisebb prioritással elküldenie a munkát.</span><span class="sxs-lookup"><span data-stu-id="3c328-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="3c328-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c328-112">PARAMETERS</span></span>

### <span data-ttu-id="3c328-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="3c328-113">-Account</span></span>
<span data-ttu-id="3c328-114">Annak a fióknak a neve, amely frissíti a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="3c328-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="3c328-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="3c328-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="3c328-116">A párhuzamosságok maximálisan támogatott foka ebben a házirendben.</span><span class="sxs-lookup"><span data-stu-id="3c328-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="3c328-117">Ezt, MinPriorityPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="3c328-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="3c328-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="3c328-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="3c328-119">A házirendre vonatkozó, a minimálisan támogatott prioritás.</span><span class="sxs-lookup"><span data-stu-id="3c328-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="3c328-120">Ezt, MaxDegreeOfParallelismPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="3c328-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="3c328-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c328-121">-Name</span></span>
<span data-ttu-id="3c328-122">Annak a számítási házirendnek a neve, amelyet frissíteni szeretne.</span><span class="sxs-lookup"><span data-stu-id="3c328-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="3c328-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c328-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c328-124">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="3c328-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3c328-125">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="3c328-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3c328-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c328-126">-Confirm</span></span>
<span data-ttu-id="3c328-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c328-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c328-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c328-128">-WhatIf</span></span>
<span data-ttu-id="3c328-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c328-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c328-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c328-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c328-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c328-131">-DefaultProfile</span></span>
<span data-ttu-id="3c328-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c328-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c328-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c328-133">CommonParameters</span></span>
<span data-ttu-id="3c328-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c328-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c328-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c328-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c328-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c328-136">INPUTS</span></span>

### <span data-ttu-id="3c328-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3c328-137">System.String</span></span>
<span data-ttu-id="3c328-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3c328-138">System.Int32</span></span>

## <span data-ttu-id="3c328-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c328-139">OUTPUTS</span></span>

### <span data-ttu-id="3c328-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c328-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c328-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c328-141">NOTES</span></span>

## <span data-ttu-id="3c328-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c328-142">RELATED LINKS</span></span>

