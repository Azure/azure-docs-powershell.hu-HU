---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298076"
---
# <span data-ttu-id="8001e-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8001e-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8001e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8001e-102">SYNOPSIS</span></span>
<span data-ttu-id="8001e-103">Adattó-adatkezelési fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8001e-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8001e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8001e-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8001e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8001e-105">DESCRIPTION</span></span>
<span data-ttu-id="8001e-106">A **New-AzDataLakeAnalyticsAccount** parancsmag az Azure Data Lake-tó Analytics-fiókját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8001e-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8001e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8001e-107">EXAMPLES</span></span>

### <span data-ttu-id="8001e-108">Példa 1: Data Lake Analytics-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="8001e-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="8001e-109">Ez a parancs létrehoz egy ContosoAdlAccount nevű adattó-fiókot, amely az ContosoAdlStore-adattárolót használja a ContosoOrg nevű erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="8001e-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="8001e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8001e-110">PARAMETERS</span></span>

### <span data-ttu-id="8001e-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8001e-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="8001e-112">Az adattó-tároló fiók nevét adja meg alapértelmezett adatforrásként.</span><span class="sxs-lookup"><span data-stu-id="8001e-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="8001e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8001e-113">-DefaultProfile</span></span>
<span data-ttu-id="8001e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8001e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8001e-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="8001e-115">-Location</span></span>
<span data-ttu-id="8001e-116">Azt a helyet adja meg, ahol az adattó-adatkezelési fiók hozható létre.</span><span class="sxs-lookup"><span data-stu-id="8001e-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="8001e-117">Jelenleg csak a kelet-amerikai 2 támogatott.</span><span class="sxs-lookup"><span data-stu-id="8001e-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="8001e-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="8001e-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="8001e-119">A választható maximálisan támogatott elemzési egységek ehhez a fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="8001e-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="8001e-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8001e-120">-MaxJobCount</span></span>
<span data-ttu-id="8001e-121">A fiók alatt futó, nem kötelezően támogatott maximális feladatok.</span><span class="sxs-lookup"><span data-stu-id="8001e-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="8001e-122">Ha nincs megadva, az alapértelmezett érték 3</span><span class="sxs-lookup"><span data-stu-id="8001e-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="8001e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8001e-123">-Name</span></span>
<span data-ttu-id="8001e-124">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8001e-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8001e-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="8001e-125">-QueryStoreRetention</span></span>
<span data-ttu-id="8001e-126">A feladat metaadatainak megőrzésére szolgáló napok tetszőleges száma.</span><span class="sxs-lookup"><span data-stu-id="8001e-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="8001e-127">Ha nincs megadva, az alapértelmezett érték 30 nap.</span><span class="sxs-lookup"><span data-stu-id="8001e-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="8001e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8001e-128">-ResourceGroupName</span></span>
<span data-ttu-id="8001e-129">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8001e-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="8001e-130">Erőforráscsoport létrehozásához használja az New-AzResourceGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8001e-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="8001e-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="8001e-131">-Tag</span></span>
<span data-ttu-id="8001e-132">A fiókkal társított címkék karakterlánca, karakterlánc-szótára</span><span class="sxs-lookup"><span data-stu-id="8001e-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="8001e-133">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="8001e-133">-Tier</span></span>
<span data-ttu-id="8001e-134">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="8001e-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="8001e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8001e-135">CommonParameters</span></span>
<span data-ttu-id="8001e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8001e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8001e-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8001e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8001e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8001e-138">INPUTS</span></span>

### <span data-ttu-id="8001e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8001e-139">System.String</span></span>

### <span data-ttu-id="8001e-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8001e-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8001e-141">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8001e-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8001e-142">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. models. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8001e-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8001e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8001e-143">OUTPUTS</span></span>

### <span data-ttu-id="8001e-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8001e-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8001e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8001e-145">NOTES</span></span>

## <span data-ttu-id="8001e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8001e-146">RELATED LINKS</span></span>

[<span data-ttu-id="8001e-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8001e-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8001e-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8001e-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8001e-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8001e-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8001e-150">Teszt-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8001e-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


