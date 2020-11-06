---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 1f2fe13567bd17170fd73854ce5554a693210c7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494533"
---
# <span data-ttu-id="3eb6b-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3eb6b-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="3eb6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3eb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb6b-103">Adatforrást ad hozzá az adattó-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3eb6b-104">SYNTAX</span></span>

### <span data-ttu-id="3eb6b-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3eb6b-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eb6b-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3eb6b-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb6b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3eb6b-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb6b-108">Az **Add-AzureRmDataLakeAnalyticsDataSource** parancsmag adatforrást ad az Azure Data Lake-tó Analytics-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3eb6b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3eb6b-109">EXAMPLES</span></span>

### <span data-ttu-id="3eb6b-110">1. példa: adatforrás felvétele egy fiókba</span><span class="sxs-lookup"><span data-stu-id="3eb6b-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="3eb6b-111">Ez a parancs egy adattó-tároló adatforrást ad az adattó-adatforráshoz az adattó-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="3eb6b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3eb6b-112">PARAMETERS</span></span>

### <span data-ttu-id="3eb6b-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="3eb6b-113">-AccessKey</span></span>
<span data-ttu-id="3eb6b-114">Megadja az Azure Blob-tároló fiók elérési kulcsát a hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb6b-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="3eb6b-115">-Account</span></span>
<span data-ttu-id="3eb6b-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb6b-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="3eb6b-117">-Blob</span></span>
<span data-ttu-id="3eb6b-118">A hozzáadni kívánt Azure Blob-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb6b-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3eb6b-119">-DataLakeStore</span></span>
<span data-ttu-id="3eb6b-120">A hozzáadandó Azure Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb6b-121">-DefaultProfile</span></span>
<span data-ttu-id="3eb6b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3eb6b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eb6b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb6b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3eb6b-124">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb6b-125">CommonParameters</span></span>
<span data-ttu-id="3eb6b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3eb6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb6b-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb6b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb6b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb6b-128">INPUTS</span></span>

### <span data-ttu-id="3eb6b-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="3eb6b-129">None</span></span>
<span data-ttu-id="3eb6b-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3eb6b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3eb6b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb6b-131">OUTPUTS</span></span>

### <span data-ttu-id="3eb6b-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="3eb6b-132">None</span></span>

## <span data-ttu-id="3eb6b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3eb6b-133">NOTES</span></span>

## <span data-ttu-id="3eb6b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eb6b-134">RELATED LINKS</span></span>

[<span data-ttu-id="3eb6b-135">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3eb6b-135">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="3eb6b-136">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3eb6b-136">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


