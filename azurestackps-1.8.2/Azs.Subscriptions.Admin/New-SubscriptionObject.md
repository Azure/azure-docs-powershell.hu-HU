---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017163"
---
# <span data-ttu-id="e79fa-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="e79fa-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="e79fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e79fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e79fa-103">A támogatott műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="e79fa-103">List of supported operations.</span></span>

## <span data-ttu-id="e79fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e79fa-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e79fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e79fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e79fa-106">A támogatott műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="e79fa-106">List of supported operations.</span></span>

## <span data-ttu-id="e79fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e79fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e79fa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e79fa-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e79fa-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="e79fa-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e79fa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e79fa-110">PARAMETERS</span></span>

### <span data-ttu-id="e79fa-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e79fa-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e79fa-112">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="e79fa-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e79fa-113">-DisplayName</span></span>
<span data-ttu-id="e79fa-114">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="e79fa-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e79fa-115">-ExternalReferenceId</span></span>
<span data-ttu-id="e79fa-116">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="e79fa-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e79fa-117">-Id</span></span>
<span data-ttu-id="e79fa-118">Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="e79fa-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e79fa-119">-Name</span></span>
<span data-ttu-id="e79fa-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e79fa-120">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e79fa-121">-OfferId</span></span>
<span data-ttu-id="e79fa-122">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="e79fa-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-123">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="e79fa-123">-Owner</span></span>
<span data-ttu-id="e79fa-124">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="e79fa-124">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e79fa-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e79fa-126">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="e79fa-126">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-127">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e79fa-127">-State</span></span>
<span data-ttu-id="e79fa-128">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="e79fa-128">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e79fa-129">-SubscriptionId</span></span>
<span data-ttu-id="e79fa-130">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e79fa-130">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79fa-131">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="e79fa-131">-TenantId</span></span>
<span data-ttu-id="e79fa-132">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="e79fa-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="e79fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79fa-133">CommonParameters</span></span>
<span data-ttu-id="e79fa-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e79fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79fa-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e79fa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79fa-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79fa-136">INPUTS</span></span>

## <span data-ttu-id="e79fa-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79fa-137">OUTPUTS</span></span>

## <span data-ttu-id="e79fa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e79fa-138">NOTES</span></span>

## <span data-ttu-id="e79fa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e79fa-139">RELATED LINKS</span></span>

