---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f415da1d6f9bb086d796c0c1bf191282c2880a09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671692"
---
# <span data-ttu-id="68bfe-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="68bfe-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="68bfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="68bfe-103">Előfizetések áthelyezése a meghatalmazott szolgáltató által kínált ajánlatok között</span><span class="sxs-lookup"><span data-stu-id="68bfe-103">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="68bfe-104">Ez a folyamat csak a márkanevet fogja elvégezni, a mögöttes ajánlat, a tervek, az előfizetések kvótája nem változik.</span><span class="sxs-lookup"><span data-stu-id="68bfe-104">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="68bfe-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68bfe-105">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="68bfe-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="68bfe-106">DESCRIPTION</span></span>
<span data-ttu-id="68bfe-107">Előfizetések áthelyezése a meghatalmazott szolgáltató által kínált ajánlatok között</span><span class="sxs-lookup"><span data-stu-id="68bfe-107">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="68bfe-108">Ez a folyamat csak a márkanevet fogja elvégezni, a mögöttes ajánlat, a tervek, az előfizetések kvótája nem változik.</span><span class="sxs-lookup"><span data-stu-id="68bfe-108">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="68bfe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="68bfe-109">EXAMPLES</span></span>

### <span data-ttu-id="68bfe-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="68bfe-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="68bfe-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/Ro1"-ResourceId "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="68bfe-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="68bfe-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="68bfe-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="68bfe-113">$resourceIds = Get-AzsUserSubscription-szűrő "offerName EQ ' O1 '" | where {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty azonosító Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="68bfe-113">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="68bfe-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68bfe-114">PARAMETERS</span></span>

### <span data-ttu-id="68bfe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68bfe-115">-AsJob</span></span>
<span data-ttu-id="68bfe-116">Azt adja meg, hogy az áthelyezési műveletet feladatként szeretné-e végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="68bfe-116">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="68bfe-117">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="68bfe-117">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="68bfe-118">A teljes mértékben minősített delegált szolgáltatót adja meg, amelybe a parancsmag áthelyezi az előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="68bfe-118">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="68bfe-119">NULL, ha az előfizetéseket az alapértelmezett szolgáltatónál vissza szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="68bfe-119">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="68bfe-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68bfe-120">-ResourceId</span></span>
<span data-ttu-id="68bfe-121">A parancsmag által áthelyezett teljes mértékben minősített előfizetési erőforrás-azonosítók sorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68bfe-121">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="68bfe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68bfe-122">CommonParameters</span></span>
<span data-ttu-id="68bfe-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68bfe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68bfe-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68bfe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68bfe-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68bfe-125">INPUTS</span></span>

## <span data-ttu-id="68bfe-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68bfe-126">OUTPUTS</span></span>

## <span data-ttu-id="68bfe-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68bfe-127">NOTES</span></span>

## <span data-ttu-id="68bfe-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68bfe-128">RELATED LINKS</span></span>

