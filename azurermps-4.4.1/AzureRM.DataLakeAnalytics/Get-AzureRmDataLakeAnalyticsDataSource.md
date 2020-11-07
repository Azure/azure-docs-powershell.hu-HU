---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680576"
---
# <span data-ttu-id="7bb5a-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bb5a-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="7bb5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bb5a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb5a-103">Adatforrást kap az adattó-adatforrásból.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bb5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bb5a-104">SYNTAX</span></span>

### <span data-ttu-id="7bb5a-105">Az összes adatforrás listázása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7bb5a-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bb5a-106">Adattároló-tároló fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="7bb5a-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bb5a-107">BLOB-tároló fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="7bb5a-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bb5a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bb5a-108">DESCRIPTION</span></span>
<span data-ttu-id="7bb5a-109">A **Get-AzureRmDataLakeAnalyticsDataSource** parancsmag Azure Data Lake Analytics-adatforrást kap.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="7bb5a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7bb5a-110">EXAMPLES</span></span>

### <span data-ttu-id="7bb5a-111">Példa 1: adatforrás kérése egy fiókból</span><span class="sxs-lookup"><span data-stu-id="7bb5a-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="7bb5a-112">Ez a parancs adattó-tároló adatforrást kap a ContosoAdls nevű adatforrásból egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="7bb5a-113">2. példa: az adattó-áruház fiókjainak listája az adattó-adatkezelési fiókban</span><span class="sxs-lookup"><span data-stu-id="7bb5a-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="7bb5a-114">Ez a parancs minden adattó-áruház fiókjait átveszi egy adattói Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7bb5a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bb5a-115">PARAMETERS</span></span>

### <span data-ttu-id="7bb5a-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="7bb5a-116">-Account</span></span>
<span data-ttu-id="7bb5a-117">Itt adhatja meg az adatforrást, amely a parancsmag által az adatforrásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="7bb5a-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="7bb5a-118">-Blob</span></span>
<span data-ttu-id="7bb5a-119">Az Azure Blob-tároló adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb5a-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7bb5a-120">-DataLakeStore</span></span>
<span data-ttu-id="7bb5a-121">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7bb5a-123">Az adatforrás nevét tartalmazó erőforráscsoport-név.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-123">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="7bb5a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb5a-124">-DefaultProfile</span></span>
<span data-ttu-id="7bb5a-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb5a-126">CommonParameters</span></span>
<span data-ttu-id="7bb5a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bb5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb5a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb5a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb5a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bb5a-129">INPUTS</span></span>

## <span data-ttu-id="7bb5a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bb5a-130">OUTPUTS</span></span>

### <span data-ttu-id="7bb5a-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="7bb5a-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="7bb5a-132">A megadott Azure Storage Account details.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="7bb5a-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="7bb5a-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="7bb5a-134">A megadott Data Lake Store-fiók adatai</span><span class="sxs-lookup"><span data-stu-id="7bb5a-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="7bb5a-135">Lista<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="7bb5a-135">List<AdlDataSource></span></span>
<span data-ttu-id="7bb5a-136">Az Azure Storage-fiókok és az adattó-tároló fiókjainak listája a megadott Data Lake Analytics-fiókban.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="7bb5a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bb5a-137">NOTES</span></span>

## <span data-ttu-id="7bb5a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bb5a-138">RELATED LINKS</span></span>

[<span data-ttu-id="7bb5a-139">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bb5a-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7bb5a-140">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bb5a-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7bb5a-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bb5a-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


