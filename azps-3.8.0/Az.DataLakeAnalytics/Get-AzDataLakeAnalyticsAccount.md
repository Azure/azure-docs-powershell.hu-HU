---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012797"
---
# <span data-ttu-id="f982b-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f982b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f982b-102">SYNOPSIS</span></span>
<span data-ttu-id="f982b-103">Információt kap az adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="f982b-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f982b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f982b-104">SYNTAX</span></span>

### <span data-ttu-id="f982b-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f982b-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f982b-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f982b-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f982b-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f982b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f982b-108">DESCRIPTION</span></span>
<span data-ttu-id="f982b-109">A **Get-AzDataLakeAnalyticsAccount** parancsmag információkat kap az Azure-alapú adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="f982b-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f982b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f982b-110">EXAMPLES</span></span>

### <span data-ttu-id="f982b-111">1. példa: adatok beolvasása az adattó Analytics-fiókjával</span><span class="sxs-lookup"><span data-stu-id="f982b-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f982b-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="f982b-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="f982b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f982b-113">PARAMETERS</span></span>

### <span data-ttu-id="f982b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f982b-114">-DefaultProfile</span></span>
<span data-ttu-id="f982b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f982b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f982b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f982b-116">-Name</span></span>
<span data-ttu-id="f982b-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f982b-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f982b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f982b-118">-ResourceGroupName</span></span>
<span data-ttu-id="f982b-119">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f982b-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f982b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f982b-120">CommonParameters</span></span>
<span data-ttu-id="f982b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f982b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f982b-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f982b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f982b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f982b-123">INPUTS</span></span>

### <span data-ttu-id="f982b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f982b-124">System.String</span></span>

## <span data-ttu-id="f982b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f982b-125">OUTPUTS</span></span>

### <span data-ttu-id="f982b-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="f982b-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="f982b-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="f982b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f982b-128">NOTES</span></span>

## <span data-ttu-id="f982b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f982b-129">RELATED LINKS</span></span>

[<span data-ttu-id="f982b-130">Új – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f982b-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f982b-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f982b-133">Teszt-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f982b-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


