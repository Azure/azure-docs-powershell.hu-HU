---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329909"
---
# <span data-ttu-id="65223-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="65223-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="65223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65223-102">SYNOPSIS</span></span>
<span data-ttu-id="65223-103">Frissítéseket vagy ajánlatokat hoz létre a privát áruházhoz.</span><span class="sxs-lookup"><span data-stu-id="65223-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="65223-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65223-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65223-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65223-105">DESCRIPTION</span></span>
<span data-ttu-id="65223-106">A bérlői webhelyen létrehozott privát áruház frissítéseit vagy ajánlatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="65223-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="65223-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65223-107">EXAMPLES</span></span>

### <span data-ttu-id="65223-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="65223-108">Example 1</span></span>
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

<span data-ttu-id="65223-109">Privát + nyilvános csomagokat hoz létre a bérlői webhelyen létrehozott privát áruházhoz.</span><span class="sxs-lookup"><span data-stu-id="65223-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="65223-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="65223-110">Example 2</span></span>
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

<span data-ttu-id="65223-111">Privát csomagokkal ajánlatokat hoz létre csak az előfizetési hatókör alatt létrehozott privát áruházhoz.</span><span class="sxs-lookup"><span data-stu-id="65223-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="65223-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="65223-112">Example 3</span></span>
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

<span data-ttu-id="65223-113">A frissítések privát + nyilvános csomagokat kínálnak a bérlői webhelyen létrehozott privát áruházhoz.</span><span class="sxs-lookup"><span data-stu-id="65223-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="65223-114">Etag szükséges.</span><span class="sxs-lookup"><span data-stu-id="65223-114">Etag is needed.</span></span>

### <span data-ttu-id="65223-115">4. példa</span><span class="sxs-lookup"><span data-stu-id="65223-115">Example 4</span></span>
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

<span data-ttu-id="65223-116">Csak az előfizetési hatókör alatt létrehozott privát csomagokkal kapcsolatos frissítéseket ajánlunk a privát áruházhoz.</span><span class="sxs-lookup"><span data-stu-id="65223-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="65223-117">Etag szükséges.</span><span class="sxs-lookup"><span data-stu-id="65223-117">Etag is needed.</span></span>


## <span data-ttu-id="65223-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65223-118">PARAMETERS</span></span>

### <span data-ttu-id="65223-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65223-119">-DefaultProfile</span></span>
<span data-ttu-id="65223-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65223-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65223-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="65223-121">-ETag</span></span>
<span data-ttu-id="65223-122">Azure Marketplace privateStore offer's eTag for update</span><span class="sxs-lookup"><span data-stu-id="65223-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="65223-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="65223-123">-OfferId</span></span>
<span data-ttu-id="65223-124">Kötelező Azure Piactér privátStore-ajánlat</span><span class="sxs-lookup"><span data-stu-id="65223-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="65223-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="65223-125">-PrivateStoreId</span></span>
<span data-ttu-id="65223-126">Kötelező Azure Piactér privátStore-ajánlatok</span><span class="sxs-lookup"><span data-stu-id="65223-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="65223-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="65223-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="65223-128">Az Azure Piactér privátStore-ajánlat konkrét csomagazonosítóira vonatkozó korlátozás</span><span class="sxs-lookup"><span data-stu-id="65223-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="65223-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65223-129">-Confirm</span></span>
<span data-ttu-id="65223-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65223-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65223-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65223-131">-WhatIf</span></span>
<span data-ttu-id="65223-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65223-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65223-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65223-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65223-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65223-134">CommonParameters</span></span>
<span data-ttu-id="65223-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65223-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65223-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65223-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65223-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65223-137">INPUTS</span></span>

### <span data-ttu-id="65223-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="65223-138">None</span></span>

## <span data-ttu-id="65223-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65223-139">OUTPUTS</span></span>

### <span data-ttu-id="65223-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="65223-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="65223-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65223-141">NOTES</span></span>

## <span data-ttu-id="65223-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65223-142">RELATED LINKS</span></span>
