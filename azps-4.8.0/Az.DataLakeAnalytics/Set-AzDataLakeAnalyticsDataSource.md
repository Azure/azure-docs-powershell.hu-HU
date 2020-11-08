---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185032"
---
# <span data-ttu-id="99be4-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="99be4-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="99be4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99be4-102">SYNOPSIS</span></span>
<span data-ttu-id="99be4-103">Módosította az adatforrások adatait az adattó Analytics-fiókjában.</span><span class="sxs-lookup"><span data-stu-id="99be4-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="99be4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99be4-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99be4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99be4-105">DESCRIPTION</span></span>
<span data-ttu-id="99be4-106">A **set-AzDataLakeAnalyticsDataSource** parancsmag módosította az Azure Data-tó Analytics-fiókja adatforrásának adatait.</span><span class="sxs-lookup"><span data-stu-id="99be4-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="99be4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99be4-107">EXAMPLES</span></span>

### <span data-ttu-id="99be4-108">Példa 1: adatforrás elérési kulcsának módosítása</span><span class="sxs-lookup"><span data-stu-id="99be4-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="99be4-109">Ez a parancs megváltoztatja az Azure Blob-adatforrások adatforrása által tárolt Access-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="99be4-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="99be4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99be4-110">PARAMETERS</span></span>

### <span data-ttu-id="99be4-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="99be4-111">-AccessKey</span></span>
<span data-ttu-id="99be4-112">Az Azure Blob-tároló adatforrás új Access-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="99be4-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="99be4-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="99be4-113">-Account</span></span>
<span data-ttu-id="99be4-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99be4-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="99be4-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="99be4-115">-Blob</span></span>
<span data-ttu-id="99be4-116">Az Azure Blob-tároló adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99be4-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="99be4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99be4-117">-DefaultProfile</span></span>
<span data-ttu-id="99be4-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="99be4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99be4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99be4-119">-ResourceGroupName</span></span>
<span data-ttu-id="99be4-120">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99be4-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="99be4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99be4-121">CommonParameters</span></span>
<span data-ttu-id="99be4-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99be4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99be4-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99be4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99be4-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99be4-124">INPUTS</span></span>

### <span data-ttu-id="99be4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="99be4-125">System.String</span></span>

## <span data-ttu-id="99be4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99be4-126">OUTPUTS</span></span>

### <span data-ttu-id="99be4-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="99be4-127">System.Void</span></span>

## <span data-ttu-id="99be4-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99be4-128">NOTES</span></span>

## <span data-ttu-id="99be4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99be4-129">RELATED LINKS</span></span>

[<span data-ttu-id="99be4-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="99be4-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="99be4-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="99be4-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


