---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504183"
---
# <span data-ttu-id="2f556-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2f556-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="2f556-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f556-102">SYNOPSIS</span></span>
<span data-ttu-id="2f556-103">Adattó-adatkezelési fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2f556-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f556-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f556-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f556-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f556-105">DESCRIPTION</span></span>
<span data-ttu-id="2f556-106">A **New-AzureRmDataLakeAnalyticsAccount** parancsmag az Azure Data Lake-tó Analytics-fiókját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2f556-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2f556-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f556-107">EXAMPLES</span></span>

### <span data-ttu-id="2f556-108">Példa 1: Data Lake Analytics-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f556-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="2f556-109">Ez a parancs létrehoz egy ContosoAdlAccount nevű adattó-fiókot, amely az ContosoAdlStore-adattárolót használja a ContosoOrg nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="2f556-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="2f556-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f556-110">PARAMETERS</span></span>

### <span data-ttu-id="2f556-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2f556-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="2f556-112">Az adattó-tároló fiók nevét adja meg alapértelmezett adatforrásként.</span><span class="sxs-lookup"><span data-stu-id="2f556-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f556-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="2f556-113">-Location</span></span>
<span data-ttu-id="2f556-114">Azt a helyet adja meg, ahol az adattó-adatkezelési fiók hozható létre.</span><span class="sxs-lookup"><span data-stu-id="2f556-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="2f556-115">Jelenleg csak a kelet-amerikai 2 támogatott.</span><span class="sxs-lookup"><span data-stu-id="2f556-115">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f556-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="2f556-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="2f556-117">A párhuzamosságok maximálisan támogatott foka ebben a fiókban.</span><span class="sxs-lookup"><span data-stu-id="2f556-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="2f556-118">Ha nincs megadva, az alapértelmezett érték 30</span><span class="sxs-lookup"><span data-stu-id="2f556-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="2f556-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="2f556-119">-MaxJobCount</span></span>
<span data-ttu-id="2f556-120">A fiók alatt futó, nem kötelezően támogatott maximális feladatok.</span><span class="sxs-lookup"><span data-stu-id="2f556-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="2f556-121">Ha nincs megadva, az alapértelmezett érték 3</span><span class="sxs-lookup"><span data-stu-id="2f556-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="2f556-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f556-122">-Name</span></span>
<span data-ttu-id="2f556-123">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f556-123">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f556-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="2f556-124">-QueryStoreRetention</span></span>
<span data-ttu-id="2f556-125">A feladat metaadatainak megőrzésére szolgáló napok tetszőleges száma.</span><span class="sxs-lookup"><span data-stu-id="2f556-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="2f556-126">Ha nincs megadva, az alapértelmezett érték 30 nap.</span><span class="sxs-lookup"><span data-stu-id="2f556-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="2f556-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f556-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f556-128">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f556-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="2f556-129">Erőforráscsoport létrehozásához használja az New-AzureRmResourceGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f556-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f556-130">-Címkék</span><span class="sxs-lookup"><span data-stu-id="2f556-130">-Tags</span></span>
<span data-ttu-id="2f556-131">Azokat a kulcs-érték párokat adja meg, amelyek a többi Azure-erőforrás között a Data Lake Analytics-fiók felismerésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="2f556-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f556-132">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="2f556-132">-Tier</span></span>
<span data-ttu-id="2f556-133">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="2f556-133">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f556-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f556-134">-DefaultProfile</span></span>
<span data-ttu-id="2f556-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f556-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f556-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f556-136">CommonParameters</span></span>
<span data-ttu-id="2f556-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f556-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f556-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f556-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f556-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f556-139">INPUTS</span></span>

## <span data-ttu-id="2f556-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f556-140">OUTPUTS</span></span>

### <span data-ttu-id="2f556-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2f556-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="2f556-142">Az újonnan létrehozott fiók részletei.</span><span class="sxs-lookup"><span data-stu-id="2f556-142">The details of the newly created account.</span></span>

## <span data-ttu-id="2f556-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f556-143">NOTES</span></span>

## <span data-ttu-id="2f556-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f556-144">RELATED LINKS</span></span>

[<span data-ttu-id="2f556-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2f556-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2f556-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2f556-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2f556-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2f556-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2f556-148">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2f556-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)

