---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194607"
---
# <span data-ttu-id="0e38e-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="0e38e-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="0e38e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e38e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e38e-103">A privát áruház frissítései vagy a felajánlás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="0e38e-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="0e38e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e38e-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e38e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e38e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e38e-106">A bérlői hatókör csoportban létrehozott privát áruház frissítéseinek vagy ajánlatának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="0e38e-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="0e38e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0e38e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e38e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0e38e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="0e38e-109">Az ajánlat létrehozása a bérlői hatókör csoportban létrehozott privát és nyilvános csomagokhoz</span><span class="sxs-lookup"><span data-stu-id="0e38e-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="0e38e-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0e38e-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="0e38e-111">Privát csomagokat hoz létre kizárólag az előfizetés hatóköre alatt létrehozott privát áruházhoz.</span><span class="sxs-lookup"><span data-stu-id="0e38e-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="0e38e-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="0e38e-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="0e38e-113">A privát áruházban a bérlői hatókör csoportban létrehozott privát és nyilvános csomagokra vonatkozó frissítéseket is kínálnak.</span><span class="sxs-lookup"><span data-stu-id="0e38e-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="0e38e-114">ETAG van szükség.</span><span class="sxs-lookup"><span data-stu-id="0e38e-114">Etag is needed.</span></span>

### <span data-ttu-id="0e38e-115">4. példa</span><span class="sxs-lookup"><span data-stu-id="0e38e-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="0e38e-116">Az előfizetés hatóköre csoportban létrehozott privát csomagokkal kapcsolatos frissítések</span><span class="sxs-lookup"><span data-stu-id="0e38e-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="0e38e-117">ETAG van szükség.</span><span class="sxs-lookup"><span data-stu-id="0e38e-117">Etag is needed.</span></span>


## <span data-ttu-id="0e38e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e38e-118">PARAMETERS</span></span>

### <span data-ttu-id="0e38e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e38e-119">-DefaultProfile</span></span>
<span data-ttu-id="0e38e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e38e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e38e-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="0e38e-121">-ETag</span></span>
<span data-ttu-id="0e38e-122">Azure Marketplace privateStore Offer 's eTag for Update</span><span class="sxs-lookup"><span data-stu-id="0e38e-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="0e38e-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="0e38e-123">-OfferId</span></span>
<span data-ttu-id="0e38e-124">Szükséges Azure Marketplace privateStore ajánlat</span><span class="sxs-lookup"><span data-stu-id="0e38e-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="0e38e-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="0e38e-125">-PrivateStoreId</span></span>
<span data-ttu-id="0e38e-126">Szükséges Azure Marketplace privateStore-ajánlatok</span><span class="sxs-lookup"><span data-stu-id="0e38e-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="0e38e-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="0e38e-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="0e38e-128">Szükséges Azure Marketplace privateStore az ajánlat konkrét terv azonosítójának korlátozásával</span><span class="sxs-lookup"><span data-stu-id="0e38e-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e38e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e38e-129">-Confirm</span></span>
<span data-ttu-id="0e38e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e38e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e38e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e38e-131">-WhatIf</span></span>
<span data-ttu-id="0e38e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e38e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e38e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e38e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e38e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e38e-134">CommonParameters</span></span>
<span data-ttu-id="0e38e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e38e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e38e-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e38e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e38e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e38e-137">INPUTS</span></span>

### <span data-ttu-id="0e38e-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e38e-138">None</span></span>

## <span data-ttu-id="0e38e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e38e-139">OUTPUTS</span></span>

### <span data-ttu-id="0e38e-140">Microsoft. Azure. Command. Marketplace. models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="0e38e-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="0e38e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e38e-141">NOTES</span></span>

## <span data-ttu-id="0e38e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e38e-142">RELATED LINKS</span></span>
