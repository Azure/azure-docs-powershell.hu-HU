---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494529"
---
# <span data-ttu-id="65445-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="65445-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="65445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65445-102">SYNOPSIS</span></span>
<span data-ttu-id="65445-103">Adattó-adatkezelési fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="65445-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65445-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65445-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65445-105">DESCRIPTION</span></span>
<span data-ttu-id="65445-106">A **New-AzureRmDataLakeAnalyticsAccount** parancsmag az Azure Data Lake-tó Analytics-fiókját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="65445-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="65445-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65445-107">EXAMPLES</span></span>

### <span data-ttu-id="65445-108">Példa 1: Data Lake Analytics-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="65445-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="65445-109">Ez a parancs létrehoz egy ContosoAdlAccount nevű adattó-fiókot, amely az ContosoAdlStore-adattárolót használja a ContosoOrg nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="65445-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="65445-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65445-110">PARAMETERS</span></span>

### <span data-ttu-id="65445-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65445-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="65445-112">Az adattó-tároló fiók nevét adja meg alapértelmezett adatforrásként.</span><span class="sxs-lookup"><span data-stu-id="65445-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65445-113">-DefaultProfile</span></span>
<span data-ttu-id="65445-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65445-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65445-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="65445-115">-Location</span></span>
<span data-ttu-id="65445-116">Azt a helyet adja meg, ahol az adattó-adatkezelési fiók hozható létre.</span><span class="sxs-lookup"><span data-stu-id="65445-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="65445-117">Jelenleg csak a kelet-amerikai 2 támogatott.</span><span class="sxs-lookup"><span data-stu-id="65445-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="65445-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="65445-119">A választható maximálisan támogatott elemzési egységek ehhez a fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="65445-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="65445-120">-MaxJobCount</span></span>
<span data-ttu-id="65445-121">A fiók alatt futó, nem kötelezően támogatott maximális feladatok.</span><span class="sxs-lookup"><span data-stu-id="65445-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="65445-122">Ha nincs megadva, az alapértelmezett érték 3</span><span class="sxs-lookup"><span data-stu-id="65445-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65445-123">-Name</span></span>
<span data-ttu-id="65445-124">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65445-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="65445-125">-QueryStoreRetention</span></span>
<span data-ttu-id="65445-126">A feladat metaadatainak megőrzésére szolgáló napok tetszőleges száma.</span><span class="sxs-lookup"><span data-stu-id="65445-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="65445-127">Ha nincs megadva, az alapértelmezett érték 30 nap.</span><span class="sxs-lookup"><span data-stu-id="65445-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65445-128">-ResourceGroupName</span></span>
<span data-ttu-id="65445-129">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65445-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="65445-130">Erőforráscsoport létrehozásához használja az New-AzureRmResourceGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="65445-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="65445-131">-Tag</span></span>
<span data-ttu-id="65445-132">A fiókkal társított címkék karakterlánca, karakterlánc-szótára</span><span class="sxs-lookup"><span data-stu-id="65445-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-133">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="65445-133">-Tier</span></span>
<span data-ttu-id="65445-134">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="65445-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65445-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65445-135">CommonParameters</span></span>
<span data-ttu-id="65445-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65445-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65445-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65445-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65445-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65445-138">INPUTS</span></span>

### <span data-ttu-id="65445-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="65445-139">None</span></span>
<span data-ttu-id="65445-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="65445-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65445-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65445-141">OUTPUTS</span></span>

### <span data-ttu-id="65445-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="65445-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="65445-143">Az újonnan létrehozott fiók részletei.</span><span class="sxs-lookup"><span data-stu-id="65445-143">The details of the newly created account.</span></span>

## <span data-ttu-id="65445-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65445-144">NOTES</span></span>

## <span data-ttu-id="65445-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65445-145">RELATED LINKS</span></span>

[<span data-ttu-id="65445-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="65445-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="65445-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="65445-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="65445-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="65445-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="65445-149">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="65445-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


