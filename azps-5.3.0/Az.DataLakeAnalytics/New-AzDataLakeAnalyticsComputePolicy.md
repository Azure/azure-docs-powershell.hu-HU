---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465868"
---
# <span data-ttu-id="856fe-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="856fe-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="856fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="856fe-102">SYNOPSIS</span></span>
<span data-ttu-id="856fe-103">Adattavak-elemzési számítási házirendszabályt hoz létre egy adott AAD-entitáshoz.</span><span class="sxs-lookup"><span data-stu-id="856fe-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="856fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="856fe-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="856fe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="856fe-105">DESCRIPTION</span></span>
<span data-ttu-id="856fe-106">A **New-AzDataLakeAnalyticsComputePolicy** létrehozza a megadott számítási házirendszabályt egy Adott AAD-entitáshoz egy Azure Data Lake Analytics-fiókban.</span><span class="sxs-lookup"><span data-stu-id="856fe-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="856fe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="856fe-107">EXAMPLES</span></span>

### <span data-ttu-id="856fe-108">1. példa: Számítási házirend létrehozása egyetlen s szabálysal</span><span class="sxs-lookup"><span data-stu-id="856fe-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="856fe-109">Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú felhasználóhoz, amely biztosítja, hogy 5 elemzési egységnél több feladatot ne tudjanak be nyújtani.</span><span class="sxs-lookup"><span data-stu-id="856fe-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="856fe-110">2. példa: Számítási házirend létrehozása mindkét szabály beállításával</span><span class="sxs-lookup"><span data-stu-id="856fe-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="856fe-111">Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú felhasználóhoz, amely biztosítja, hogy ne tudjanak 5-5 elemzési egységnél több vagy 100-asnál kisebb prioritású feladatot be nyújtani.</span><span class="sxs-lookup"><span data-stu-id="856fe-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="856fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="856fe-112">PARAMETERS</span></span>

### <span data-ttu-id="856fe-113">-Account</span><span class="sxs-lookup"><span data-stu-id="856fe-113">-Account</span></span>
<span data-ttu-id="856fe-114">Annak a fióknak a neve, amelybe fel szeretné venni a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="856fe-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="856fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856fe-115">-DefaultProfile</span></span>
<span data-ttu-id="856fe-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="856fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="856fe-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="856fe-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="856fe-118">A házirendhez a maximális támogatott elemzési egység egy feladathoz.</span><span class="sxs-lookup"><span data-stu-id="856fe-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="856fe-119">Ezt vagy a MinPriorityPerJob paramétert, vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="856fe-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="856fe-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="856fe-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="856fe-121">A házirend minimális támogatott prioritása feladatonként.</span><span class="sxs-lookup"><span data-stu-id="856fe-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="856fe-122">Ezt vagy a MaxAnalyticsUnitsPerJob paramétert, vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="856fe-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="856fe-123">-Name</span><span class="sxs-lookup"><span data-stu-id="856fe-123">-Name</span></span>
<span data-ttu-id="856fe-124">A létrehozni szükséges számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="856fe-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="856fe-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="856fe-125">-ObjectId</span></span>
<span data-ttu-id="856fe-126">Annak a felhasználónak vagy csoportnak az Azure Active Directory-objektumazonosítója, akire a házirendet alkalmazni kell.</span><span class="sxs-lookup"><span data-stu-id="856fe-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="856fe-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="856fe-127">-ObjectType</span></span>
<span data-ttu-id="856fe-128">A átadott objektumazonosító Azure Active Directory-objektumtípusa.</span><span class="sxs-lookup"><span data-stu-id="856fe-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="856fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="856fe-130">Annak az erőforráscsoportnak a neve, amely alatt a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="856fe-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="856fe-131">Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="856fe-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="856fe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="856fe-132">-Confirm</span></span>
<span data-ttu-id="856fe-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="856fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856fe-134">-WhatIf</span></span>
<span data-ttu-id="856fe-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="856fe-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="856fe-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="856fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856fe-137">CommonParameters</span></span>
<span data-ttu-id="856fe-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856fe-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856fe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856fe-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="856fe-140">INPUTS</span></span>

### <span data-ttu-id="856fe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="856fe-141">System.String</span></span>

### <span data-ttu-id="856fe-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="856fe-142">System.Guid</span></span>

### <span data-ttu-id="856fe-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="856fe-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="856fe-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="856fe-144">OUTPUTS</span></span>

### <span data-ttu-id="856fe-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="856fe-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="856fe-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="856fe-146">NOTES</span></span>

## <span data-ttu-id="856fe-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="856fe-147">RELATED LINKS</span></span>
