---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370031"
---
# <span data-ttu-id="d7afb-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d7afb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7afb-102">SYNOPSIS</span></span>
<span data-ttu-id="d7afb-103">Információkat kap egy Data Lake Analytics-fiókról.</span><span class="sxs-lookup"><span data-stu-id="d7afb-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d7afb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7afb-104">SYNTAX</span></span>

### <span data-ttu-id="d7afb-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7afb-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7afb-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d7afb-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7afb-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7afb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7afb-108">DESCRIPTION</span></span>
<span data-ttu-id="d7afb-109">A **Get-AzDataLakeAnalyticsAccount** parancsmag információkat kap egy Azure Data Lake Analytics-fiókról.</span><span class="sxs-lookup"><span data-stu-id="d7afb-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d7afb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7afb-110">EXAMPLES</span></span>

### <span data-ttu-id="d7afb-111">1. példa: Adatok lekérte a Data Lake Analytics-fiók adatait</span><span class="sxs-lookup"><span data-stu-id="d7afb-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d7afb-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="d7afb-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="d7afb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7afb-113">PARAMETERS</span></span>

### <span data-ttu-id="d7afb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7afb-114">-DefaultProfile</span></span>
<span data-ttu-id="d7afb-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7afb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7afb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d7afb-116">-Name</span></span>
<span data-ttu-id="d7afb-117">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7afb-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7afb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7afb-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7afb-119">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7afb-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7afb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7afb-120">CommonParameters</span></span>
<span data-ttu-id="d7afb-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7afb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7afb-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7afb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7afb-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7afb-123">INPUTS</span></span>

### <span data-ttu-id="d7afb-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d7afb-124">System.String</span></span>

## <span data-ttu-id="d7afb-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7afb-125">OUTPUTS</span></span>

### <span data-ttu-id="d7afb-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="d7afb-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="d7afb-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="d7afb-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7afb-128">NOTES</span></span>

## <span data-ttu-id="d7afb-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7afb-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7afb-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d7afb-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d7afb-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d7afb-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d7afb-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


