---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679478"
---
# <span data-ttu-id="2ade3-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2ade3-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="2ade3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ade3-102">SYNOPSIS</span></span>
<span data-ttu-id="2ade3-103">Módosította az adatforrások adatait az adattó Analytics-fiókjában.</span><span class="sxs-lookup"><span data-stu-id="2ade3-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ade3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ade3-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ade3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ade3-105">DESCRIPTION</span></span>
<span data-ttu-id="2ade3-106">A **set-AzureRmDataLakeAnalyticsDataSource** parancsmag módosította az Azure Data-tó Analytics-fiókja adatforrásának adatait.</span><span class="sxs-lookup"><span data-stu-id="2ade3-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2ade3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2ade3-107">EXAMPLES</span></span>

### <span data-ttu-id="2ade3-108">Példa 1: adatforrás elérési kulcsának módosítása</span><span class="sxs-lookup"><span data-stu-id="2ade3-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="2ade3-109">Ez a parancs megváltoztatja az Azure Blob-adatforrások adatforrása által tárolt Access-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="2ade3-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="2ade3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ade3-110">PARAMETERS</span></span>

### <span data-ttu-id="2ade3-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="2ade3-111">-AccessKey</span></span>
<span data-ttu-id="2ade3-112">Az Azure Blob-tároló adatforrás új Access-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ade3-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="2ade3-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="2ade3-113">-Account</span></span>
<span data-ttu-id="2ade3-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ade3-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2ade3-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2ade3-115">-Blob</span></span>
<span data-ttu-id="2ade3-116">Az Azure Blob-tároló adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ade3-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ade3-117">-ResourceGroupName</span></span>
<span data-ttu-id="2ade3-118">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ade3-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="2ade3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ade3-119">-DefaultProfile</span></span>
<span data-ttu-id="2ade3-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ade3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ade3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ade3-121">CommonParameters</span></span>
<span data-ttu-id="2ade3-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ade3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ade3-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ade3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ade3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ade3-124">INPUTS</span></span>

## <span data-ttu-id="2ade3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ade3-125">OUTPUTS</span></span>

### <span data-ttu-id="2ade3-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ade3-126">None</span></span>

## <span data-ttu-id="2ade3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ade3-127">NOTES</span></span>

## <span data-ttu-id="2ade3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ade3-128">RELATED LINKS</span></span>

[<span data-ttu-id="2ade3-129">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2ade3-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="2ade3-130">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2ade3-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


