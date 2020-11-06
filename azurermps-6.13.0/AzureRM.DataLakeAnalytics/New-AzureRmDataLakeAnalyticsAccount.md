---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502132"
---
# <span data-ttu-id="d1224-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d1224-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d1224-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1224-102">SYNOPSIS</span></span>
<span data-ttu-id="d1224-103">Adattó-adatkezelési fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d1224-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1224-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1224-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1224-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1224-105">DESCRIPTION</span></span>
<span data-ttu-id="d1224-106">A **New-AzureRmDataLakeAnalyticsAccount** parancsmag az Azure Data Lake-tó Analytics-fiókját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d1224-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d1224-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1224-107">EXAMPLES</span></span>

### <span data-ttu-id="d1224-108">Példa 1: Data Lake Analytics-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="d1224-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="d1224-109">Ez a parancs létrehoz egy ContosoAdlAccount nevű adattó-fiókot, amely az ContosoAdlStore-adattárolót használja a ContosoOrg nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="d1224-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="d1224-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1224-110">PARAMETERS</span></span>

### <span data-ttu-id="d1224-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1224-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="d1224-112">Az adattó-tároló fiók nevét adja meg alapértelmezett adatforrásként.</span><span class="sxs-lookup"><span data-stu-id="d1224-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="d1224-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1224-113">-DefaultProfile</span></span>
<span data-ttu-id="d1224-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d1224-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1224-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="d1224-115">-Location</span></span>
<span data-ttu-id="d1224-116">Azt a helyet adja meg, ahol az adattó-adatkezelési fiók hozható létre.</span><span class="sxs-lookup"><span data-stu-id="d1224-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="d1224-117">Jelenleg csak a kelet-amerikai 2 támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1224-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="d1224-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="d1224-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="d1224-119">A választható maximálisan támogatott elemzési egységek ehhez a fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d1224-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1224-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d1224-120">-MaxJobCount</span></span>
<span data-ttu-id="d1224-121">A fiók alatt futó, nem kötelezően támogatott maximális feladatok.</span><span class="sxs-lookup"><span data-stu-id="d1224-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="d1224-122">Ha nincs megadva, az alapértelmezett érték 3</span><span class="sxs-lookup"><span data-stu-id="d1224-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="d1224-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1224-123">-Name</span></span>
<span data-ttu-id="d1224-124">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1224-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d1224-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="d1224-125">-QueryStoreRetention</span></span>
<span data-ttu-id="d1224-126">A feladat metaadatainak megőrzésére szolgáló napok tetszőleges száma.</span><span class="sxs-lookup"><span data-stu-id="d1224-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="d1224-127">Ha nincs megadva, az alapértelmezett érték 30 nap.</span><span class="sxs-lookup"><span data-stu-id="d1224-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="d1224-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1224-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1224-129">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1224-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="d1224-130">Erőforráscsoport létrehozásához használja az New-AzureRmResourceGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d1224-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="d1224-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="d1224-131">-Tag</span></span>
<span data-ttu-id="d1224-132">A fiókkal társított címkék karakterlánca, karakterlánc-szótára</span><span class="sxs-lookup"><span data-stu-id="d1224-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="d1224-133">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="d1224-133">-Tier</span></span>
<span data-ttu-id="d1224-134">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d1224-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="d1224-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1224-135">CommonParameters</span></span>
<span data-ttu-id="d1224-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1224-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1224-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1224-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1224-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1224-138">INPUTS</span></span>

### <span data-ttu-id="d1224-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1224-139">System.String</span></span>

### <span data-ttu-id="d1224-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1224-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d1224-141">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d1224-141">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d1224-142">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. models. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d1224-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d1224-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1224-143">OUTPUTS</span></span>

### <span data-ttu-id="d1224-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d1224-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d1224-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1224-145">NOTES</span></span>

## <span data-ttu-id="d1224-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1224-146">RELATED LINKS</span></span>

[<span data-ttu-id="d1224-147">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d1224-147">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d1224-148">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d1224-148">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d1224-149">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d1224-149">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d1224-150">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d1224-150">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


