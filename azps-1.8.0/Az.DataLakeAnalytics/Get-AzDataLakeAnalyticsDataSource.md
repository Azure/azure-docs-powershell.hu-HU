---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 29f9315063db7d6bb16f8656950da39e70ddced9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836405"
---
# <span data-ttu-id="1c592-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c592-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1c592-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c592-102">SYNOPSIS</span></span>
<span data-ttu-id="1c592-103">Adatforrást kap az adattó-adatforrásból.</span><span class="sxs-lookup"><span data-stu-id="1c592-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="1c592-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c592-104">SYNTAX</span></span>

### <span data-ttu-id="1c592-105">GetAllDataSources (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c592-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c592-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c592-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c592-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c592-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c592-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c592-108">DESCRIPTION</span></span>
<span data-ttu-id="1c592-109">A **Get-AzDataLakeAnalyticsDataSource** parancsmag Azure Data Lake Analytics-adatforrást kap.</span><span class="sxs-lookup"><span data-stu-id="1c592-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="1c592-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1c592-110">EXAMPLES</span></span>

### <span data-ttu-id="1c592-111">Példa 1: adatforrás kérése egy fiókból</span><span class="sxs-lookup"><span data-stu-id="1c592-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="1c592-112">Ez a parancs adattó-tároló adatforrást kap a ContosoAdls nevű adatforrásból egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="1c592-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="1c592-113">2. példa: az adattó-áruház fiókjainak listája az adattó-adatkezelési fiókban</span><span class="sxs-lookup"><span data-stu-id="1c592-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="1c592-114">Ez a parancs minden adattó-áruház fiókjait átveszi egy adattói Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="1c592-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1c592-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c592-115">PARAMETERS</span></span>

### <span data-ttu-id="1c592-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="1c592-116">-Account</span></span>
<span data-ttu-id="1c592-117">Itt adhatja meg az adatforrást, amely a parancsmag által az adatforrásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="1c592-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="1c592-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1c592-118">-Blob</span></span>
<span data-ttu-id="1c592-119">Az Azure Blob-tároló adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c592-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c592-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c592-120">-DataLakeStore</span></span>
<span data-ttu-id="1c592-121">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c592-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c592-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c592-122">-DefaultProfile</span></span>
<span data-ttu-id="1c592-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1c592-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c592-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c592-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c592-125">Az adatforrás nevét tartalmazó erőforráscsoport-név.</span><span class="sxs-lookup"><span data-stu-id="1c592-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c592-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c592-126">CommonParameters</span></span>
<span data-ttu-id="1c592-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c592-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c592-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c592-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c592-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c592-129">INPUTS</span></span>

### <span data-ttu-id="1c592-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1c592-130">System.String</span></span>

## <span data-ttu-id="1c592-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c592-131">OUTPUTS</span></span>

### <span data-ttu-id="1c592-132">Microsoft. Azure. Command. DataLakeAnalytics. models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="1c592-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="1c592-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="1c592-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="1c592-134">Microsoft. Azure. Command. DataLakeAnalytics. models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="1c592-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="1c592-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c592-135">NOTES</span></span>

## <span data-ttu-id="1c592-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c592-136">RELATED LINKS</span></span>

[<span data-ttu-id="1c592-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c592-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1c592-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c592-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1c592-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c592-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


