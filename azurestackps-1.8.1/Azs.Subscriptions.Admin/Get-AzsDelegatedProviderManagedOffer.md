---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840519"
---
# <span data-ttu-id="e9703-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="e9703-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="e9703-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9703-102">SYNOPSIS</span></span>
<span data-ttu-id="e9703-103">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e9703-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="e9703-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9703-104">SYNTAX</span></span>

### <span data-ttu-id="e9703-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9703-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9703-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e9703-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="e9703-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9703-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e9703-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9703-108">DESCRIPTION</span></span>
<span data-ttu-id="e9703-109">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e9703-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="e9703-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e9703-110">EXAMPLES</span></span>

### <span data-ttu-id="e9703-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9703-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e9703-112">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e9703-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="e9703-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9703-113">PARAMETERS</span></span>

### <span data-ttu-id="e9703-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="e9703-114">-DelegatedProviderId</span></span>
<span data-ttu-id="e9703-115">DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e9703-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="e9703-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9703-116">-Name</span></span>
<span data-ttu-id="e9703-117">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="e9703-117">Name of an offer.</span></span>

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

### <span data-ttu-id="e9703-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9703-118">-ResourceId</span></span>
<span data-ttu-id="e9703-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e9703-119">The resource id.</span></span>

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

### <span data-ttu-id="e9703-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="e9703-120">-Skip</span></span>
<span data-ttu-id="e9703-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e9703-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e9703-122">-Top</span><span class="sxs-lookup"><span data-stu-id="e9703-122">-Top</span></span>
<span data-ttu-id="e9703-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="e9703-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9703-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="e9703-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e9703-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9703-125">CommonParameters</span></span>
<span data-ttu-id="e9703-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9703-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9703-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9703-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9703-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9703-128">INPUTS</span></span>

## <span data-ttu-id="e9703-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9703-129">OUTPUTS</span></span>

### <span data-ttu-id="e9703-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="e9703-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="e9703-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9703-131">NOTES</span></span>

## <span data-ttu-id="e9703-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9703-132">RELATED LINKS</span></span>

