---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/get-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: f23912ed21105015e69b94b27c5c5cc7899ed044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493669"
---
# <span data-ttu-id="39820-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="39820-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="39820-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39820-102">SYNOPSIS</span></span>
<span data-ttu-id="39820-103">Az adott közzétevői azonosító (közzétevő), ajánlati azonosító (PRODUCT) és Plan azonosító (név) szerződési feltételeinek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="39820-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="39820-104">Az e parancs által visszaadott kitételeket a program átadja Set-AzureRmMarketplaceTerms a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="39820-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39820-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39820-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39820-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="39820-106">DESCRIPTION</span></span>
<span data-ttu-id="39820-107">A **Get-AzureRmMarketplaceTerms** parancsmag a Publisher-azonosító (Publisher), az ajánlat-azonosító (PRODUCT) és a Plan ID (név) rekord feltételeit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="39820-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="39820-108">Példák</span><span class="sxs-lookup"><span data-stu-id="39820-108">EXAMPLES</span></span>

### <span data-ttu-id="39820-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39820-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="39820-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39820-110">PARAMETERS</span></span>

### <span data-ttu-id="39820-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39820-111">-DefaultProfile</span></span>
<span data-ttu-id="39820-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39820-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39820-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39820-113">-Name</span></span>
<span data-ttu-id="39820-114">A telepítendő kép terv azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="39820-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39820-115">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="39820-115">-Product</span></span>
<span data-ttu-id="39820-116">A telepített lemezkép azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="39820-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39820-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="39820-117">-Publisher</span></span>
<span data-ttu-id="39820-118">A telepítendő lemezkép közzétevő azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="39820-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39820-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39820-119">CommonParameters</span></span>
<span data-ttu-id="39820-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39820-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39820-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39820-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39820-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39820-122">INPUTS</span></span>

### <span data-ttu-id="39820-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="39820-123">None</span></span>

## <span data-ttu-id="39820-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39820-124">OUTPUTS</span></span>

### <span data-ttu-id="39820-125">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="39820-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="39820-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39820-126">NOTES</span></span>

## <span data-ttu-id="39820-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39820-127">RELATED LINKS</span></span>
