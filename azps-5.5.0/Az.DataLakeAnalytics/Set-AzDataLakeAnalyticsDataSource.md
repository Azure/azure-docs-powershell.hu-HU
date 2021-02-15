---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161979"
---
# <span data-ttu-id="0bc9a-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0bc9a-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="0bc9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc9a-103">Módosítja egy Data Lake Analytics-fiók adatforrásának részleteit.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0bc9a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0bc9a-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bc9a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0bc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc9a-106">A **Set-AzDataLakeAnalyticsDataSource** parancsmag módosítja egy Azure Data Lake Analytics-fiók adatforrásának részleteit.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0bc9a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0bc9a-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc9a-108">1. példa: Adatforrás hozzáférési kulcsának módosítása</span><span class="sxs-lookup"><span data-stu-id="0bc9a-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="0bc9a-109">Ez a parancs módosítja egy Azure Blob Storage-adatforrás hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="0bc9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bc9a-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc9a-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="0bc9a-111">-AccessKey</span></span>
<span data-ttu-id="0bc9a-112">Az Azure Blob Storage adatforrás új hozzáférési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="0bc9a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="0bc9a-113">-Account</span></span>
<span data-ttu-id="0bc9a-114">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0bc9a-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="0bc9a-115">-Blob</span></span>
<span data-ttu-id="0bc9a-116">Az Azure Blob Storage adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="0bc9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc9a-117">-DefaultProfile</span></span>
<span data-ttu-id="0bc9a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0bc9a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bc9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0bc9a-120">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0bc9a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc9a-121">CommonParameters</span></span>
<span data-ttu-id="0bc9a-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc9a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc9a-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc9a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc9a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bc9a-124">INPUTS</span></span>

### <span data-ttu-id="0bc9a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0bc9a-125">System.String</span></span>

## <span data-ttu-id="0bc9a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bc9a-126">OUTPUTS</span></span>

### <span data-ttu-id="0bc9a-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="0bc9a-127">System.Void</span></span>

## <span data-ttu-id="0bc9a-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0bc9a-128">NOTES</span></span>

## <span data-ttu-id="0bc9a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bc9a-129">RELATED LINKS</span></span>

[<span data-ttu-id="0bc9a-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0bc9a-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="0bc9a-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0bc9a-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


