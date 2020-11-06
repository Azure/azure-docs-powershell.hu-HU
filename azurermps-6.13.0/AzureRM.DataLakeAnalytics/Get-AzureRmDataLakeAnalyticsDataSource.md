---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2f6dfae3d13a6de57a7dc04367ec2886be78f5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502147"
---
# <span data-ttu-id="fd1d4-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd1d4-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="fd1d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1d4-103">Adatforrást kap az adattó-adatforrásból.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd1d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd1d4-104">SYNTAX</span></span>

### <span data-ttu-id="fd1d4-105">GetAllDataSources (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd1d4-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd1d4-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fd1d4-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd1d4-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd1d4-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd1d4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd1d4-108">DESCRIPTION</span></span>
<span data-ttu-id="fd1d4-109">A **Get-AzureRmDataLakeAnalyticsDataSource** parancsmag Azure Data Lake Analytics-adatforrást kap.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="fd1d4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fd1d4-110">EXAMPLES</span></span>

### <span data-ttu-id="fd1d4-111">Példa 1: adatforrás kérése egy fiókból</span><span class="sxs-lookup"><span data-stu-id="fd1d4-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="fd1d4-112">Ez a parancs adattó-tároló adatforrást kap a ContosoAdls nevű adatforrásból egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="fd1d4-113">2. példa: az adattó-áruház fiókjainak listája az adattó-adatkezelési fiókban</span><span class="sxs-lookup"><span data-stu-id="fd1d4-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="fd1d4-114">Ez a parancs minden adattó-áruház fiókjait átveszi egy adattói Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="fd1d4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd1d4-115">PARAMETERS</span></span>

### <span data-ttu-id="fd1d4-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fd1d4-116">-Account</span></span>
<span data-ttu-id="fd1d4-117">Itt adhatja meg az adatforrást, amely a parancsmag által az adatforrásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="fd1d4-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="fd1d4-118">-Blob</span></span>
<span data-ttu-id="fd1d4-119">Az Azure Blob-tároló adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="fd1d4-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fd1d4-120">-DataLakeStore</span></span>
<span data-ttu-id="fd1d4-121">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fd1d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd1d4-122">-DefaultProfile</span></span>
<span data-ttu-id="fd1d4-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd1d4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd1d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd1d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd1d4-125">Az adatforrás nevét tartalmazó erőforráscsoport-név.</span><span class="sxs-lookup"><span data-stu-id="fd1d4-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="fd1d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1d4-126">CommonParameters</span></span>
<span data-ttu-id="fd1d4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd1d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1d4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd1d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1d4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd1d4-129">INPUTS</span></span>

### <span data-ttu-id="fd1d4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd1d4-130">System.String</span></span>

## <span data-ttu-id="fd1d4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd1d4-131">OUTPUTS</span></span>

### <span data-ttu-id="fd1d4-132">Microsoft. Azure. Command. DataLakeAnalytics. models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="fd1d4-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="fd1d4-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="fd1d4-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="fd1d4-134">Microsoft. Azure. Command. DataLakeAnalytics. models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="fd1d4-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="fd1d4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd1d4-135">NOTES</span></span>

## <span data-ttu-id="fd1d4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd1d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd1d4-137">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd1d4-137">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="fd1d4-138">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd1d4-138">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="fd1d4-139">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd1d4-139">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)

