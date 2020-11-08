---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025421"
---
# <span data-ttu-id="aca4c-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="aca4c-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="aca4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aca4c-102">SYNOPSIS</span></span>
<span data-ttu-id="aca4c-103">Adatforrást ad hozzá az adattó-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="aca4c-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="aca4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aca4c-104">SYNTAX</span></span>

### <span data-ttu-id="aca4c-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aca4c-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aca4c-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aca4c-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aca4c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aca4c-107">DESCRIPTION</span></span>
<span data-ttu-id="aca4c-108">Az **Add-AzDataLakeAnalyticsDataSource** parancsmag adatforrást ad az Azure Data Lake-tó Analytics-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="aca4c-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="aca4c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aca4c-109">EXAMPLES</span></span>

### <span data-ttu-id="aca4c-110">1. példa: adatforrás felvétele egy fiókba</span><span class="sxs-lookup"><span data-stu-id="aca4c-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="aca4c-111">Ez a parancs egy adattó-tároló adatforrást ad az adattó-adatforráshoz az adattó-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="aca4c-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="aca4c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aca4c-112">PARAMETERS</span></span>

### <span data-ttu-id="aca4c-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="aca4c-113">-AccessKey</span></span>
<span data-ttu-id="aca4c-114">Megadja az Azure Blob-tároló fiók elérési kulcsát a hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="aca4c-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca4c-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="aca4c-115">-Account</span></span>
<span data-ttu-id="aca4c-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aca4c-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="aca4c-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="aca4c-117">-Blob</span></span>
<span data-ttu-id="aca4c-118">A hozzáadni kívánt Azure Blob-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aca4c-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca4c-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aca4c-119">-DataLakeStore</span></span>
<span data-ttu-id="aca4c-120">A hozzáadandó Azure Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aca4c-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca4c-121">-DefaultProfile</span></span>
<span data-ttu-id="aca4c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aca4c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aca4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="aca4c-124">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aca4c-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca4c-125">CommonParameters</span></span>
<span data-ttu-id="aca4c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aca4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca4c-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca4c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca4c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aca4c-128">INPUTS</span></span>

### <span data-ttu-id="aca4c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aca4c-129">System.String</span></span>

## <span data-ttu-id="aca4c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aca4c-130">OUTPUTS</span></span>

### <span data-ttu-id="aca4c-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="aca4c-131">System.Object</span></span>
## <span data-ttu-id="aca4c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aca4c-132">NOTES</span></span>

## <span data-ttu-id="aca4c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aca4c-133">RELATED LINKS</span></span>

[<span data-ttu-id="aca4c-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="aca4c-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="aca4c-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="aca4c-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


