---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840312"
---
# <span data-ttu-id="f3df7-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="f3df7-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="f3df7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3df7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3df7-103">Annak ellenőrzése, hogy a felhasználói előfizetések áthelyezhetők-e a delegált szolgáltató által kínált ajánlatok közé.</span><span class="sxs-lookup"><span data-stu-id="f3df7-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="f3df7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3df7-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="f3df7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3df7-105">DESCRIPTION</span></span>
<span data-ttu-id="f3df7-106">Annak ellenőrzése, hogy a felhasználói előfizetések áthelyezhetők-e a delegált szolgáltató által kínált ajánlatok közé.</span><span class="sxs-lookup"><span data-stu-id="f3df7-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="f3df7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3df7-107">EXAMPLES</span></span>

### <span data-ttu-id="f3df7-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3df7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="f3df7-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/Ro1"-ResourceId "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="f3df7-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="f3df7-110">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3df7-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="f3df7-111">$resourceIds = Get-AzsUserSubscription-szűrő "offerName EQ ' O1 '" | Select-ExpandProperty azonosító Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="f3df7-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="f3df7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3df7-112">PARAMETERS</span></span>

### <span data-ttu-id="f3df7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3df7-113">-AsJob</span></span>
<span data-ttu-id="f3df7-114">Azt adja meg, hogy az áthelyezési műveletet feladatként szeretné-e végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="f3df7-114">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3df7-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="f3df7-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="f3df7-116">A teljes mértékben minősített delegált szolgáltatót adja meg, amelybe a parancsmag áthelyezi az előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="f3df7-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="f3df7-117">NULL, ha az előfizetéseket az alapértelmezett szolgáltatónál vissza szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="f3df7-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3df7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3df7-118">-ResourceId</span></span>
<span data-ttu-id="f3df7-119">A parancsmag által áthelyezett teljes mértékben minősített előfizetési erőforrás-azonosítók sorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3df7-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3df7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3df7-120">CommonParameters</span></span>
<span data-ttu-id="f3df7-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3df7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3df7-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3df7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3df7-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3df7-123">INPUTS</span></span>

## <span data-ttu-id="f3df7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3df7-124">OUTPUTS</span></span>

## <span data-ttu-id="f3df7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3df7-125">NOTES</span></span>

## <span data-ttu-id="f3df7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3df7-126">RELATED LINKS</span></span>

