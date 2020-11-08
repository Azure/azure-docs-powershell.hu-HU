---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025662"
---
# <span data-ttu-id="d8f8f-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d8f8f-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="d8f8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f8f-103">Szerezzen be egy vagy több privát áruház ajánlatát.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="d8f8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8f8f-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f8f-106">Szerezzen be egy vagy több privát áruház ajánlatát a bérlői hatókör csoportban hozzáadott nyilvános + privát csomagokkal.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="d8f8f-107">Ha az előfizetési azonosító be van írva, csak az előfizetések hatóköre szerint szerezzen be egy vagy több magánjellegű áruház ajánlatát.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="d8f8f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d8f8f-108">EXAMPLES</span></span>

### <span data-ttu-id="d8f8f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8f8f-109">Example 1</span></span>
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

<span data-ttu-id="d8f8f-110">A privát áruházból privát és nyilvános csomagokat kaphat, amelyeket a bérlői hatókör csoportban hozzáadott.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="d8f8f-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="d8f8f-111">Example 2</span></span>
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

<span data-ttu-id="d8f8f-112">A magánjellegű áruházból kiinduló ajánlatok csak az előfizetések hatóköre alatt hozzáadott egyéni csomagokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="d8f8f-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="d8f8f-113">Example 3</span></span>
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

<span data-ttu-id="d8f8f-114">Privát áruházat kaphat a bérlői hatókör csoportban hozzáadott privát és nyilvános csomagokkal.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="d8f8f-115">4. példa</span><span class="sxs-lookup"><span data-stu-id="d8f8f-115">Example 4</span></span>
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

<span data-ttu-id="d8f8f-116">A magánjellegű áruházat csak a bérlői hatókör kategóriába felvett privát csomagokkal veheti fel.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="d8f8f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8f8f-117">PARAMETERS</span></span>

### <span data-ttu-id="d8f8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f8f-118">-DefaultProfile</span></span>
<span data-ttu-id="d8f8f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f8f-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="d8f8f-120">-OfferId</span></span>
<span data-ttu-id="d8f8f-121">Szükséges Azure Marketplace privateStore ajánlat</span><span class="sxs-lookup"><span data-stu-id="d8f8f-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="d8f8f-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="d8f8f-122">-PrivateStoreId</span></span>
<span data-ttu-id="d8f8f-123">Szükséges Azure Marketplace privateStore-ajánlatok</span><span class="sxs-lookup"><span data-stu-id="d8f8f-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="d8f8f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8f8f-124">-SubscriptionId</span></span>
<span data-ttu-id="d8f8f-125">Azure Marketplace előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="d8f8f-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="d8f8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f8f-126">CommonParameters</span></span>
<span data-ttu-id="d8f8f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8f8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f8f-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d8f8f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f8f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8f8f-129">INPUTS</span></span>

### <span data-ttu-id="d8f8f-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="d8f8f-130">None</span></span>

## <span data-ttu-id="d8f8f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8f8f-131">OUTPUTS</span></span>

### <span data-ttu-id="d8f8f-132">Microsoft. Azure. Command. Marketplace. models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d8f8f-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="d8f8f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8f8f-133">NOTES</span></span>

## <span data-ttu-id="d8f8f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8f8f-134">RELATED LINKS</span></span>
