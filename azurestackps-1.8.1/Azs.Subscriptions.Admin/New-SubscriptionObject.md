---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840469"
---
# <span data-ttu-id="059eb-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="059eb-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="059eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="059eb-102">SYNOPSIS</span></span>
<span data-ttu-id="059eb-103">A támogatott műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="059eb-103">List of supported operations.</span></span>

## <span data-ttu-id="059eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="059eb-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="059eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="059eb-105">DESCRIPTION</span></span>
<span data-ttu-id="059eb-106">A támogatott műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="059eb-106">List of supported operations.</span></span>

## <span data-ttu-id="059eb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="059eb-107">EXAMPLES</span></span>

### <span data-ttu-id="059eb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="059eb-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="059eb-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="059eb-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="059eb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="059eb-110">PARAMETERS</span></span>

### <span data-ttu-id="059eb-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="059eb-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="059eb-112">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="059eb-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="059eb-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="059eb-113">-DisplayName</span></span>
<span data-ttu-id="059eb-114">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="059eb-114">Subscription name.</span></span>

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

### <span data-ttu-id="059eb-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="059eb-115">-ExternalReferenceId</span></span>
<span data-ttu-id="059eb-116">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="059eb-116">External reference identifier.</span></span>

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

### <span data-ttu-id="059eb-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="059eb-117">-Id</span></span>
<span data-ttu-id="059eb-118">Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="059eb-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="059eb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="059eb-119">-Name</span></span>
<span data-ttu-id="059eb-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="059eb-120">Name of the resource.</span></span>

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

### <span data-ttu-id="059eb-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="059eb-121">-OfferId</span></span>
<span data-ttu-id="059eb-122">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="059eb-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="059eb-123">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="059eb-123">-Owner</span></span>
<span data-ttu-id="059eb-124">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="059eb-124">Subscription owner.</span></span>

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

### <span data-ttu-id="059eb-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="059eb-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="059eb-126">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="059eb-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="059eb-127">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="059eb-127">-State</span></span>
<span data-ttu-id="059eb-128">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="059eb-128">Subscription state.</span></span>

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

### <span data-ttu-id="059eb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="059eb-129">-SubscriptionId</span></span>
<span data-ttu-id="059eb-130">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="059eb-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="059eb-131">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="059eb-131">-TenantId</span></span>
<span data-ttu-id="059eb-132">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="059eb-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="059eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059eb-133">CommonParameters</span></span>
<span data-ttu-id="059eb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="059eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059eb-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059eb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059eb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="059eb-136">INPUTS</span></span>

## <span data-ttu-id="059eb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="059eb-137">OUTPUTS</span></span>

## <span data-ttu-id="059eb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="059eb-138">NOTES</span></span>

## <span data-ttu-id="059eb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="059eb-139">RELATED LINKS</span></span>

