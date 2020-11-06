---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493534"
---
# <span data-ttu-id="2f525-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2f525-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="2f525-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f525-102">SYNOPSIS</span></span>
<span data-ttu-id="2f525-103">Adattó-elemzést hoz létre egy bizonyos AAD-entitásra vonatkozó házirend-szabály kiszámításához.</span><span class="sxs-lookup"><span data-stu-id="2f525-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f525-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f525-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f525-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f525-105">DESCRIPTION</span></span>
<span data-ttu-id="2f525-106">A **New-AzureRmDataLakeAnalyticsComputePolicy** létrehozza a megadott számítási házirend-szabályt egy adott aad-entitáshoz egy Azure-adattó-adatkezelési fiókban.</span><span class="sxs-lookup"><span data-stu-id="2f525-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2f525-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f525-107">EXAMPLES</span></span>

### <span data-ttu-id="2f525-108">Példa 1: számítási házirend létrehozása csak egy szabállyal</span><span class="sxs-lookup"><span data-stu-id="2f525-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="2f525-109">Ez a parancs a "contosoadla" fiók "myPolicy" nevű házirendjét hozza létre a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú felhasználó számára, amely biztosítja, hogy az ötnél több mint párhuzamosan ne nyújtsanak be munkát.</span><span class="sxs-lookup"><span data-stu-id="2f525-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="2f525-110">2. példa: számítási házirend létrehozása mindkét szabállyal</span><span class="sxs-lookup"><span data-stu-id="2f525-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="2f525-111">Ez a parancs egy "myPolicy" nevű házirendet hoz létre a "contosoadla" nevű felhasználónál a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú felhasználónál, amely biztosítja, hogy az ötnél több vagy kevesebb párhuzamosságtal vagy a 100-nál kisebb prioritással ne nyújtsanak be munkát.</span><span class="sxs-lookup"><span data-stu-id="2f525-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="2f525-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f525-112">PARAMETERS</span></span>

### <span data-ttu-id="2f525-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="2f525-113">-Account</span></span>
<span data-ttu-id="2f525-114">Annak a fióknak a neve, amelyhez a számítási házirendet hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="2f525-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="2f525-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="2f525-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="2f525-116">A párhuzamosságok maximálisan támogatott foka ebben a házirendben.</span><span class="sxs-lookup"><span data-stu-id="2f525-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="2f525-117">Ezt, MinPriorityPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="2f525-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="2f525-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="2f525-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="2f525-119">A házirendre vonatkozó, a minimálisan támogatott prioritás.</span><span class="sxs-lookup"><span data-stu-id="2f525-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="2f525-120">Ezt, MaxDegreeOfParallelismPerJob vagy mindkét paramétert meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="2f525-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="2f525-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f525-121">-Name</span></span>
<span data-ttu-id="2f525-122">A létrehozandó számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="2f525-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="2f525-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2f525-123">-ObjectId</span></span>
<span data-ttu-id="2f525-124">Annak a felhasználónak vagy csoportnak az Azure Active Directory-objektum azonosítója, amelyre alkalmazni szeretné a házirendet.</span><span class="sxs-lookup"><span data-stu-id="2f525-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="2f525-125">-Objektumtípus</span><span class="sxs-lookup"><span data-stu-id="2f525-125">-ObjectType</span></span>
<span data-ttu-id="2f525-126">Az Azure Active Directory objektumtípus a beadott objektum-AZONOSÍTÓhoz.</span><span class="sxs-lookup"><span data-stu-id="2f525-126">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="2f525-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f525-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f525-128">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="2f525-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="2f525-129">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="2f525-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="2f525-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f525-130">-Confirm</span></span>
<span data-ttu-id="2f525-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f525-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f525-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f525-132">-WhatIf</span></span>
<span data-ttu-id="2f525-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f525-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f525-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f525-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f525-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f525-135">-DefaultProfile</span></span>
<span data-ttu-id="2f525-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f525-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f525-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f525-137">CommonParameters</span></span>
<span data-ttu-id="2f525-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f525-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f525-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f525-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f525-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f525-140">INPUTS</span></span>

### <span data-ttu-id="2f525-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2f525-141">System.String</span></span>
<span data-ttu-id="2f525-142">System. GUID System. Int32</span><span class="sxs-lookup"><span data-stu-id="2f525-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="2f525-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f525-143">OUTPUTS</span></span>

### <span data-ttu-id="2f525-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2f525-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="2f525-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f525-145">NOTES</span></span>

## <span data-ttu-id="2f525-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f525-146">RELATED LINKS</span></span>

