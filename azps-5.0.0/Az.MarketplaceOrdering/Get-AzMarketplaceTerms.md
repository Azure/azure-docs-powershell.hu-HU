---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194601"
---
# <span data-ttu-id="bc768-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="bc768-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="bc768-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc768-102">SYNOPSIS</span></span>
<span data-ttu-id="bc768-103">Az adott közzétevői azonosító (közzétevő), ajánlati azonosító (PRODUCT) és Plan azonosító (név) szerződési feltételeinek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="bc768-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="bc768-104">Az e parancs által visszaadott kitételeket a program átadja Set-AzMarketplaceTerms a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="bc768-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="bc768-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc768-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc768-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc768-106">DESCRIPTION</span></span>
<span data-ttu-id="bc768-107">A **Get-AzMarketplaceTerms** parancsmag a Publisher-azonosító (Publisher), az ajánlat-azonosító (PRODUCT) és a Plan ID (név) rekord feltételeit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bc768-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="bc768-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bc768-108">EXAMPLES</span></span>

### <span data-ttu-id="bc768-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bc768-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="bc768-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc768-110">PARAMETERS</span></span>

### <span data-ttu-id="bc768-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc768-111">-DefaultProfile</span></span>
<span data-ttu-id="bc768-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc768-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc768-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc768-113">-Name</span></span>
<span data-ttu-id="bc768-114">A telepítendő kép terv azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="bc768-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="bc768-115">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="bc768-115">-Product</span></span>
<span data-ttu-id="bc768-116">A telepített lemezkép azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="bc768-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="bc768-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bc768-117">-Publisher</span></span>
<span data-ttu-id="bc768-118">A telepítendő lemezkép közzétevő azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="bc768-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="bc768-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc768-119">CommonParameters</span></span>
<span data-ttu-id="bc768-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc768-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc768-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc768-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc768-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc768-122">INPUTS</span></span>

### <span data-ttu-id="bc768-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="bc768-123">None</span></span>

## <span data-ttu-id="bc768-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc768-124">OUTPUTS</span></span>

### <span data-ttu-id="bc768-125">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="bc768-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="bc768-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc768-126">NOTES</span></span>

## <span data-ttu-id="bc768-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc768-127">RELATED LINKS</span></span>