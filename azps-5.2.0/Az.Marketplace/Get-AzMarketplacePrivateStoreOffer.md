---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329886"
---
# <span data-ttu-id="a99af-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="a99af-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="a99af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a99af-102">SYNOPSIS</span></span>
<span data-ttu-id="a99af-103">Szerezze be egy vagy több privát áruház ajánlatát.</span><span class="sxs-lookup"><span data-stu-id="a99af-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="a99af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a99af-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a99af-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a99af-105">DESCRIPTION</span></span>
<span data-ttu-id="a99af-106">Egy vagy több privát áruház ajánlatának lekérte a bérlői webhelyen felvett nyilvános + privát csomagokat.</span><span class="sxs-lookup"><span data-stu-id="a99af-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="a99af-107">Ha az előfizetésazonosító ajándék, egy vagy több privát áruház ajánlatát csak az előfizetés hatóköre alatt, privát csomagokkal szerezze be.</span><span class="sxs-lookup"><span data-stu-id="a99af-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="a99af-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a99af-108">EXAMPLES</span></span>

### <span data-ttu-id="a99af-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="a99af-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="a99af-110">Privát áruházi ajánlatokat kap a bérlői körhöz hozzáadott privát + nyilvános csomagokkal.</span><span class="sxs-lookup"><span data-stu-id="a99af-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="a99af-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a99af-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="a99af-112">Privát áruházi ajánlatok csak az előfizetési hatókör alá felvett privát csomagokkal.</span><span class="sxs-lookup"><span data-stu-id="a99af-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="a99af-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="a99af-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="a99af-114">Privát áruház ajánlatának lekérte a bérlői körhöz hozzáadott privát + nyilvános csomagokat.</span><span class="sxs-lookup"><span data-stu-id="a99af-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="a99af-115">4. példa</span><span class="sxs-lookup"><span data-stu-id="a99af-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="a99af-116">Privát áruház ajánlatának lekérte csak a bérlői körhöz hozzáadott privát csomagokat.</span><span class="sxs-lookup"><span data-stu-id="a99af-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="a99af-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a99af-117">PARAMETERS</span></span>

### <span data-ttu-id="a99af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99af-118">-DefaultProfile</span></span>
<span data-ttu-id="a99af-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a99af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a99af-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="a99af-120">-OfferId</span></span>
<span data-ttu-id="a99af-121">Kötelező Azure Piactér privátStore-ajánlat</span><span class="sxs-lookup"><span data-stu-id="a99af-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99af-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="a99af-122">-PrivateStoreId</span></span>
<span data-ttu-id="a99af-123">Kötelező Azure Piactér privátStore-ajánlatok</span><span class="sxs-lookup"><span data-stu-id="a99af-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="a99af-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a99af-124">-SubscriptionId</span></span>
<span data-ttu-id="a99af-125">Azure Piactér-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="a99af-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99af-126">CommonParameters</span></span>
<span data-ttu-id="a99af-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99af-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a99af-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99af-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a99af-129">INPUTS</span></span>

### <span data-ttu-id="a99af-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="a99af-130">None</span></span>

## <span data-ttu-id="a99af-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a99af-131">OUTPUTS</span></span>

### <span data-ttu-id="a99af-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="a99af-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="a99af-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a99af-133">NOTES</span></span>

## <span data-ttu-id="a99af-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a99af-134">RELATED LINKS</span></span>
