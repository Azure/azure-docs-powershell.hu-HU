---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 016c2520ee97f03c19a68eefebdc0319bacdb6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006838"
---
# <span data-ttu-id="2f2aa-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2f2aa-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="2f2aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2aa-103">Data Lake Analytics-adatforrást kap.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="2f2aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f2aa-104">SYNTAX</span></span>

### <span data-ttu-id="2f2aa-105">GetAllDataSources (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f2aa-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f2aa-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2f2aa-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f2aa-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f2aa-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f2aa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f2aa-108">DESCRIPTION</span></span>
<span data-ttu-id="2f2aa-109">A **Get-AzDataLakeAnalyticsDataSource** parancsmag egy Azure Data Lake Analytics adatforrást kap.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="2f2aa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f2aa-110">EXAMPLES</span></span>

### <span data-ttu-id="2f2aa-111">1. példa: Adatforrás lekérte egy fiókból</span><span class="sxs-lookup"><span data-stu-id="2f2aa-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="2f2aa-112">Ez a parancs egy ContosoAdls nevű Data Lake Store-adatforrást kap egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="2f2aa-113">2. példa: A Data Lake Store-fiókok listájának lekérte egy Data Lake Analytics-fiókban</span><span class="sxs-lookup"><span data-stu-id="2f2aa-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="2f2aa-114">Ez a parancs minden Data Lake Store-fiókot lekért egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2f2aa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f2aa-115">PARAMETERS</span></span>

### <span data-ttu-id="2f2aa-116">-Account</span><span class="sxs-lookup"><span data-stu-id="2f2aa-116">-Account</span></span>
<span data-ttu-id="2f2aa-117">Azt a Data Lake Analytics-fiókot adja meg, amelyből a parancsmag adatforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="2f2aa-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="2f2aa-118">-Blob</span></span>
<span data-ttu-id="2f2aa-119">Az Azure Blob Storage adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="2f2aa-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2f2aa-120">-DataLakeStore</span></span>
<span data-ttu-id="2f2aa-121">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2f2aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2aa-122">-DefaultProfile</span></span>
<span data-ttu-id="2f2aa-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f2aa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f2aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f2aa-125">Megadja az adatforrást tartalmazó erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="2f2aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2aa-126">CommonParameters</span></span>
<span data-ttu-id="2f2aa-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2aa-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f2aa-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2aa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f2aa-129">INPUTS</span></span>

### <span data-ttu-id="2f2aa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2f2aa-130">System.String</span></span>

## <span data-ttu-id="2f2aa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f2aa-131">OUTPUTS</span></span>

### <span data-ttu-id="2f2aa-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="2f2aa-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="2f2aa-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="2f2aa-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="2f2aa-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="2f2aa-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="2f2aa-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f2aa-135">NOTES</span></span>

## <span data-ttu-id="2f2aa-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f2aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f2aa-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2f2aa-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="2f2aa-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2f2aa-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="2f2aa-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2f2aa-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


