---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016909"
---
# <span data-ttu-id="41d31-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="41d31-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="41d31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41d31-102">SYNOPSIS</span></span>
<span data-ttu-id="41d31-103">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="41d31-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="41d31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41d31-104">SYNTAX</span></span>

### <span data-ttu-id="41d31-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41d31-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="41d31-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="41d31-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="41d31-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41d31-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="41d31-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="41d31-108">DESCRIPTION</span></span>
<span data-ttu-id="41d31-109">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="41d31-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="41d31-110">Példák</span><span class="sxs-lookup"><span data-stu-id="41d31-110">EXAMPLES</span></span>

### <span data-ttu-id="41d31-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41d31-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="41d31-112">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="41d31-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="41d31-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41d31-113">PARAMETERS</span></span>

### <span data-ttu-id="41d31-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="41d31-114">-DelegatedProviderId</span></span>
<span data-ttu-id="41d31-115">DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="41d31-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d31-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41d31-116">-Name</span></span>
<span data-ttu-id="41d31-117">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="41d31-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d31-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41d31-118">-ResourceId</span></span>
<span data-ttu-id="41d31-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="41d31-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d31-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="41d31-120">-Skip</span></span>
<span data-ttu-id="41d31-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="41d31-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d31-122">-Top</span><span class="sxs-lookup"><span data-stu-id="41d31-122">-Top</span></span>
<span data-ttu-id="41d31-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="41d31-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="41d31-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="41d31-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d31-125">CommonParameters</span></span>
<span data-ttu-id="41d31-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41d31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d31-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d31-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d31-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41d31-128">INPUTS</span></span>

## <span data-ttu-id="41d31-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41d31-129">OUTPUTS</span></span>

### <span data-ttu-id="41d31-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="41d31-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="41d31-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41d31-131">NOTES</span></span>

## <span data-ttu-id="41d31-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41d31-132">RELATED LINKS</span></span>

