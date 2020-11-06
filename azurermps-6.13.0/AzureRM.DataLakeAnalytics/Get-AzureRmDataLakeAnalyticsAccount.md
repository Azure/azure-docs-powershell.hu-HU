---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 32c7478e7e2419a8f83c839efd841f25446a96c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494079"
---
# <span data-ttu-id="c1c3b-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c1c3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c3b-103">Információt kap az adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="c1c3b-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1c3b-104">SYNTAX</span></span>

### <span data-ttu-id="c1c3b-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1c3b-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1c3b-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1c3b-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1c3b-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c3b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1c3b-108">DESCRIPTION</span></span>
<span data-ttu-id="c1c3b-109">A **Get-AzureRmDataLakeAnalyticsAccount** parancsmag információkat kap az Azure-alapú adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="c1c3b-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c1c3b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c1c3b-110">EXAMPLES</span></span>

### <span data-ttu-id="c1c3b-111">1. példa: adatok beolvasása az adattó Analytics-fiókjával</span><span class="sxs-lookup"><span data-stu-id="c1c3b-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="c1c3b-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="c1c3b-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="c1c3b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1c3b-113">PARAMETERS</span></span>

### <span data-ttu-id="c1c3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c3b-114">-DefaultProfile</span></span>
<span data-ttu-id="c1c3b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c1c3b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c3b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1c3b-116">-Name</span></span>
<span data-ttu-id="c1c3b-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c3b-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c1c3b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c3b-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1c3b-119">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c3b-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c1c3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c3b-120">CommonParameters</span></span>
<span data-ttu-id="c1c3b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1c3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c3b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c3b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c3b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c3b-123">INPUTS</span></span>

### <span data-ttu-id="c1c3b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c3b-124">System.String</span></span>

## <span data-ttu-id="c1c3b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c3b-125">OUTPUTS</span></span>

### <span data-ttu-id="c1c3b-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c1c3b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1c3b-127">NOTES</span></span>

## <span data-ttu-id="c1c3b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1c3b-128">RELATED LINKS</span></span>

[<span data-ttu-id="c1c3b-129">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c1c3b-130">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-130">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c1c3b-131">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-131">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c1c3b-132">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1c3b-132">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


