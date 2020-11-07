---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840482"
---
# <span data-ttu-id="ffdbf-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="ffdbf-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="ffdbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdbf-103">Delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="ffdbf-103">Offer delegation.</span></span>

## <span data-ttu-id="ffdbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffdbf-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ffdbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffdbf-105">DESCRIPTION</span></span>
<span data-ttu-id="ffdbf-106">Delegált ajánlat</span><span class="sxs-lookup"><span data-stu-id="ffdbf-106">Offer delegation.</span></span>

## <span data-ttu-id="ffdbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ffdbf-107">EXAMPLES</span></span>

### <span data-ttu-id="ffdbf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ffdbf-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ffdbf-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="ffdbf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ffdbf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffdbf-110">PARAMETERS</span></span>

### <span data-ttu-id="ffdbf-111">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ffdbf-111">-Id</span></span>
<span data-ttu-id="ffdbf-112">Az erőforrás URI-ja.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-112">URI of the resource.</span></span>

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

### <span data-ttu-id="ffdbf-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="ffdbf-113">-Location</span></span>
<span data-ttu-id="ffdbf-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-114">Location of the resource.</span></span>

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

### <span data-ttu-id="ffdbf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffdbf-115">-Name</span></span>
<span data-ttu-id="ffdbf-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-116">Name of the resource.</span></span>

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

### <span data-ttu-id="ffdbf-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffdbf-117">-SubscriptionId</span></span>
<span data-ttu-id="ffdbf-118">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="ffdbf-119">-Címkék</span><span class="sxs-lookup"><span data-stu-id="ffdbf-119">-Tags</span></span>
<span data-ttu-id="ffdbf-120">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffdbf-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ffdbf-121">-Type</span></span>
<span data-ttu-id="ffdbf-122">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-122">Type of resource.</span></span>

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

### <span data-ttu-id="ffdbf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdbf-123">CommonParameters</span></span>
<span data-ttu-id="ffdbf-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffdbf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdbf-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffdbf-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdbf-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffdbf-126">INPUTS</span></span>

## <span data-ttu-id="ffdbf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffdbf-127">OUTPUTS</span></span>

## <span data-ttu-id="ffdbf-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffdbf-128">NOTES</span></span>

## <span data-ttu-id="ffdbf-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffdbf-129">RELATED LINKS</span></span>

