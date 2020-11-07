---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840483"
---
# <span data-ttu-id="611da-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="611da-101">New-OfferObject</span></span>

## <span data-ttu-id="611da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="611da-102">SYNOPSIS</span></span>
<span data-ttu-id="611da-103">Azoknak a szolgáltatásoknak a felajánlását jelenti, amelyekhez előfizetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="611da-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="611da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="611da-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="611da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="611da-105">DESCRIPTION</span></span>
<span data-ttu-id="611da-106">Azoknak a szolgáltatásoknak a felajánlását jelenti, amelyekhez előfizetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="611da-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="611da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="611da-107">EXAMPLES</span></span>

### <span data-ttu-id="611da-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="611da-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="611da-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="611da-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="611da-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="611da-110">PARAMETERS</span></span>

### <span data-ttu-id="611da-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="611da-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="611da-112">Azon bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint tud beszerezni.</span><span class="sxs-lookup"><span data-stu-id="611da-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611da-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="611da-113">-BasePlanIds</span></span>
<span data-ttu-id="611da-114">Azoknak az alapterveknek az azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="611da-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611da-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="611da-115">-Description</span></span>
<span data-ttu-id="611da-116">Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="611da-116">Description of offer.</span></span>

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

### <span data-ttu-id="611da-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="611da-117">-DisplayName</span></span>
<span data-ttu-id="611da-118">Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="611da-118">Display name of offer.</span></span>

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

### <span data-ttu-id="611da-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="611da-119">-ExternalReferenceId</span></span>
<span data-ttu-id="611da-120">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="611da-120">External reference identifier.</span></span>

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

### <span data-ttu-id="611da-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="611da-121">-Id</span></span>
<span data-ttu-id="611da-122">Az erőforrás URI-ja.</span><span class="sxs-lookup"><span data-stu-id="611da-122">URI of the resource.</span></span>

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

### <span data-ttu-id="611da-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="611da-123">-Location</span></span>
<span data-ttu-id="611da-124">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="611da-124">Location where resource is location.</span></span>

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

### <span data-ttu-id="611da-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="611da-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="611da-126">Fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="611da-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611da-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="611da-127">-Name</span></span>
<span data-ttu-id="611da-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="611da-128">Name of the resource.</span></span>

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

### <span data-ttu-id="611da-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="611da-129">-State</span></span>
<span data-ttu-id="611da-130">Kisegítő lehetőségek állapota</span><span class="sxs-lookup"><span data-stu-id="611da-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="611da-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="611da-131">-SubscriptionCount</span></span>
<span data-ttu-id="611da-132">Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="611da-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611da-133">-Címkék</span><span class="sxs-lookup"><span data-stu-id="611da-133">-Tags</span></span>
<span data-ttu-id="611da-134">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="611da-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611da-135">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="611da-135">-Type</span></span>
<span data-ttu-id="611da-136">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="611da-136">Type of resource.</span></span>

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

### <span data-ttu-id="611da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611da-137">CommonParameters</span></span>
<span data-ttu-id="611da-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="611da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611da-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="611da-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611da-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="611da-140">INPUTS</span></span>

## <span data-ttu-id="611da-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="611da-141">OUTPUTS</span></span>

## <span data-ttu-id="611da-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="611da-142">NOTES</span></span>

## <span data-ttu-id="611da-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="611da-143">RELATED LINKS</span></span>

