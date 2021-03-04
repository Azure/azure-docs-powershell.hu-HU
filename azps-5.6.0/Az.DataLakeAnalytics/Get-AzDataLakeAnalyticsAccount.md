---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: dcd44f9b43184ffc36d58bd5b65a065d7e81b4b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925002"
---
# <span data-ttu-id="0b9cf-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0b9cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9cf-103">Információkat kap egy Data Lake Analytics-fiókról.</span><span class="sxs-lookup"><span data-stu-id="0b9cf-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0b9cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b9cf-104">SYNTAX</span></span>

### <span data-ttu-id="0b9cf-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b9cf-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b9cf-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b9cf-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b9cf-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b9cf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b9cf-108">DESCRIPTION</span></span>
<span data-ttu-id="0b9cf-109">A **Get-AzDataLakeAnalyticsAccount** parancsmag információkat kap egy Azure Data Lake Analytics-fiókról.</span><span class="sxs-lookup"><span data-stu-id="0b9cf-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0b9cf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b9cf-110">EXAMPLES</span></span>

### <span data-ttu-id="0b9cf-111">1. példa: Adatok lekérdezése a Data Lake Analytics-fiókról</span><span class="sxs-lookup"><span data-stu-id="0b9cf-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0b9cf-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="0b9cf-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="0b9cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b9cf-113">PARAMETERS</span></span>

### <span data-ttu-id="0b9cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9cf-114">-DefaultProfile</span></span>
<span data-ttu-id="0b9cf-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0b9cf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b9cf-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0b9cf-116">-Name</span></span>
<span data-ttu-id="0b9cf-117">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b9cf-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0b9cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b9cf-119">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b9cf-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0b9cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9cf-120">CommonParameters</span></span>
<span data-ttu-id="0b9cf-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b9cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9cf-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b9cf-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9cf-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b9cf-123">INPUTS</span></span>

### <span data-ttu-id="0b9cf-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0b9cf-124">System.String</span></span>

## <span data-ttu-id="0b9cf-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b9cf-125">OUTPUTS</span></span>

### <span data-ttu-id="0b9cf-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="0b9cf-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="0b9cf-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="0b9cf-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b9cf-128">NOTES</span></span>

## <span data-ttu-id="0b9cf-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b9cf-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b9cf-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0b9cf-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0b9cf-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0b9cf-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b9cf-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


