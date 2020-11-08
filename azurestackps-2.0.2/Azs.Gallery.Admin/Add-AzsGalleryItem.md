---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016807"
---
# <span data-ttu-id="b38a1-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b38a1-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="b38a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b38a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b38a1-103">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="b38a1-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="b38a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b38a1-104">SYNTAX</span></span>

### <span data-ttu-id="b38a1-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b38a1-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b38a1-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="b38a1-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b38a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b38a1-107">DESCRIPTION</span></span>
<span data-ttu-id="b38a1-108">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="b38a1-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="b38a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b38a1-109">EXAMPLES</span></span>

### <span data-ttu-id="b38a1-110">Példa 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b38a1-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="b38a1-111">Feltöltések TestUbuntu. teszt. 1.0.0 a gyűjteménybe.</span><span class="sxs-lookup"><span data-stu-id="b38a1-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="b38a1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b38a1-112">PARAMETERS</span></span>

### <span data-ttu-id="b38a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38a1-113">-DefaultProfile</span></span>
<span data-ttu-id="b38a1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b38a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b38a1-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="b38a1-115">-GalleryItemUri</span></span>
<span data-ttu-id="b38a1-116">Az online-ra feltöltött gyűjtemény-csomag URI-ja.</span><span class="sxs-lookup"><span data-stu-id="b38a1-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b38a1-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="b38a1-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="b38a1-118">A gyűjtemény elemeinek tárolási helye.</span><span class="sxs-lookup"><span data-stu-id="b38a1-118">Location of gallery item payload.</span></span>
<span data-ttu-id="b38a1-119">A kivitelezéshez tekintse meg a GALLERYITEMURIPAYLOAD tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b38a1-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b38a1-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b38a1-120">-SubscriptionId</span></span>
<span data-ttu-id="b38a1-121">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b38a1-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b38a1-122">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b38a1-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b38a1-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b38a1-123">-Confirm</span></span>
<span data-ttu-id="b38a1-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b38a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b38a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b38a1-125">-WhatIf</span></span>
<span data-ttu-id="b38a1-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b38a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b38a1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b38a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b38a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38a1-128">CommonParameters</span></span>
<span data-ttu-id="b38a1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b38a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38a1-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b38a1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38a1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b38a1-131">INPUTS</span></span>

### <span data-ttu-id="b38a1-132">Microsoft. Azure. PowerShell. parancsmagok. Gallery. models. Api20150401. IGalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="b38a1-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="b38a1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b38a1-133">OUTPUTS</span></span>

### <span data-ttu-id="b38a1-134">Microsoft. Azure. PowerShell. parancsmagok. Gallery. models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b38a1-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="b38a1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b38a1-135">NOTES</span></span>

<span data-ttu-id="b38a1-136">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b38a1-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b38a1-137">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b38a1-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b38a1-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : a gyűjteményben található elemek tartalma.</span><span class="sxs-lookup"><span data-stu-id="b38a1-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="b38a1-139">`[GalleryItemUri <String>]`: A már online feltöltött gyűjtemény-csomag URI-ja.</span><span class="sxs-lookup"><span data-stu-id="b38a1-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="b38a1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b38a1-140">RELATED LINKS</span></span>

