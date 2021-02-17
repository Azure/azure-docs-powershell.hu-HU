---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147491"
---
# <span data-ttu-id="571f5-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="571f5-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="571f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="571f5-102">SYNOPSIS</span></span>
<span data-ttu-id="571f5-103">Szerezze be egy adott közzétevő-azonosító(Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) szerződési feltételeit.</span><span class="sxs-lookup"><span data-stu-id="571f5-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="571f5-104">A jelen parancs által visszaadott kifejezésobjektumot át kell Set-AzMarketplaceTerms a jogi feltételek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="571f5-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="571f5-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="571f5-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="571f5-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="571f5-106">DESCRIPTION</span></span>
<span data-ttu-id="571f5-107">A **Get-AzMarketplaceTerms** parancsmag visszaadja az adott közzétevő-azonosító(Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) rekord feltételeit.</span><span class="sxs-lookup"><span data-stu-id="571f5-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="571f5-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="571f5-108">EXAMPLES</span></span>

### <span data-ttu-id="571f5-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="571f5-109">Example 1</span></span>
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

## <span data-ttu-id="571f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="571f5-110">PARAMETERS</span></span>

### <span data-ttu-id="571f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571f5-111">-DefaultProfile</span></span>
<span data-ttu-id="571f5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="571f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="571f5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="571f5-113">-Name</span></span>
<span data-ttu-id="571f5-114">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="571f5-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="571f5-115">-Product</span><span class="sxs-lookup"><span data-stu-id="571f5-115">-Product</span></span>
<span data-ttu-id="571f5-116">Offer identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="571f5-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="571f5-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="571f5-117">-Publisher</span></span>
<span data-ttu-id="571f5-118">Publisher identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="571f5-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="571f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571f5-119">CommonParameters</span></span>
<span data-ttu-id="571f5-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="571f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571f5-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571f5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571f5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="571f5-122">INPUTS</span></span>

### <span data-ttu-id="571f5-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="571f5-123">None</span></span>

## <span data-ttu-id="571f5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="571f5-124">OUTPUTS</span></span>

### <span data-ttu-id="571f5-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="571f5-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="571f5-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="571f5-126">NOTES</span></span>

## <span data-ttu-id="571f5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="571f5-127">RELATED LINKS</span></span>
