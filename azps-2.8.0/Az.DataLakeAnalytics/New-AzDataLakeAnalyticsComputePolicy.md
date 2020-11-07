---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 3fbf0d09b2307d96512c04e13521544a69fcde8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666907"
---
# <span data-ttu-id="782b4-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="782b4-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="782b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="782b4-102">SYNOPSIS</span></span>
<span data-ttu-id="782b4-103">Adattó-elemzést hoz létre egy bizonyos AAD-entitásra vonatkozó házirend-szabály kiszámításához.</span><span class="sxs-lookup"><span data-stu-id="782b4-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="782b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="782b4-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="782b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="782b4-105">DESCRIPTION</span></span>
<span data-ttu-id="782b4-106">A **New-AzDataLakeAnalyticsComputePolicy** létrehozza a megadott számítási házirend-szabályt egy adott aad-entitáshoz egy Azure-adattó-adatkezelési fiókban.</span><span class="sxs-lookup"><span data-stu-id="782b4-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="782b4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="782b4-107">EXAMPLES</span></span>

### <span data-ttu-id="782b4-108">Példa 1: számítási házirend létrehozása csak egy szabállyal</span><span class="sxs-lookup"><span data-stu-id="782b4-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="782b4-109">Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" nevű felhasználónál a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú felhasználónál, amely biztosítja, hogy az ötnél több adategységgel nem tud semmilyen munkát beküldenie.</span><span class="sxs-lookup"><span data-stu-id="782b4-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="782b4-110">2. példa: számítási házirend létrehozása mindkét szabállyal</span><span class="sxs-lookup"><span data-stu-id="782b4-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="782b4-111">Ez a parancs egy "myPolicy" nevű házirendet hoz létre a "contosoadla" nevű felhasználónál a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú felhasználónál, amely biztosítja, hogy a felhasználó nem tud több mint 5 Analytics-egységgel vagy a 100-nál kisebb prioritással elküldenie a munkát.</span><span class="sxs-lookup"><span data-stu-id="782b4-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="782b4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="782b4-112">PARAMETERS</span></span>

### <span data-ttu-id="782b4-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="782b4-113">-Account</span></span>
<span data-ttu-id="782b4-114">Annak a fióknak a neve, amelyhez a számítási házirendet hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="782b4-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="782b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782b4-115">-DefaultProfile</span></span>
<span data-ttu-id="782b4-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="782b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="782b4-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="782b4-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="782b4-118">A házirendben a maximálisan támogatott elemzési egységek száma.</span><span class="sxs-lookup"><span data-stu-id="782b4-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="782b4-119">Ezt, MinPriorityPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="782b4-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="782b4-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="782b4-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="782b4-121">A házirendre vonatkozó, a minimálisan támogatott prioritás.</span><span class="sxs-lookup"><span data-stu-id="782b4-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="782b4-122">Ezt, MaxAnalyticsUnitsPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="782b4-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="782b4-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="782b4-123">-Name</span></span>
<span data-ttu-id="782b4-124">A létrehozandó számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="782b4-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="782b4-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="782b4-125">-ObjectId</span></span>
<span data-ttu-id="782b4-126">Annak a felhasználónak vagy csoportnak az Azure Active Directory-objektum azonosítója, amelyre alkalmazni szeretné a házirendet.</span><span class="sxs-lookup"><span data-stu-id="782b4-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="782b4-127">-Objektumtípus</span><span class="sxs-lookup"><span data-stu-id="782b4-127">-ObjectType</span></span>
<span data-ttu-id="782b4-128">Az Azure Active Directory objektumtípus a beadott objektum-AZONOSÍTÓhoz.</span><span class="sxs-lookup"><span data-stu-id="782b4-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="782b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="782b4-130">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="782b4-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="782b4-131">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="782b4-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="782b4-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="782b4-132">-Confirm</span></span>
<span data-ttu-id="782b4-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="782b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782b4-134">-WhatIf</span></span>
<span data-ttu-id="782b4-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="782b4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="782b4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="782b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782b4-137">CommonParameters</span></span>
<span data-ttu-id="782b4-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="782b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782b4-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="782b4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782b4-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="782b4-140">INPUTS</span></span>

### <span data-ttu-id="782b4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="782b4-141">System.String</span></span>

### <span data-ttu-id="782b4-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="782b4-142">System.Guid</span></span>

### <span data-ttu-id="782b4-143">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="782b4-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="782b4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="782b4-144">OUTPUTS</span></span>

### <span data-ttu-id="782b4-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="782b4-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="782b4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="782b4-146">NOTES</span></span>

## <span data-ttu-id="782b4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="782b4-147">RELATED LINKS</span></span>
