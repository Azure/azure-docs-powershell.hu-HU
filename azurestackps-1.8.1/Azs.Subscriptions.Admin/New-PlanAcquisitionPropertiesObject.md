---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840481"
---
# <span data-ttu-id="48e53-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="48e53-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="48e53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48e53-102">SYNOPSIS</span></span>
<span data-ttu-id="48e53-103">Az előfizetéshez tartozó bővítmény-terv megvásárlását jelöli.</span><span class="sxs-lookup"><span data-stu-id="48e53-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="48e53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48e53-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="48e53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48e53-105">DESCRIPTION</span></span>
<span data-ttu-id="48e53-106">Az előfizetéshez tartozó bővítmény-terv megvásárlását jelöli.</span><span class="sxs-lookup"><span data-stu-id="48e53-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="48e53-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48e53-107">EXAMPLES</span></span>

### <span data-ttu-id="48e53-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48e53-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="48e53-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="48e53-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="48e53-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48e53-110">PARAMETERS</span></span>

### <span data-ttu-id="48e53-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="48e53-111">-AcquisitionId</span></span>
<span data-ttu-id="48e53-112">A beszerzési azonosító.</span><span class="sxs-lookup"><span data-stu-id="48e53-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="48e53-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="48e53-113">-AcquisitionTime</span></span>
<span data-ttu-id="48e53-114">Akvizíciós idő.</span><span class="sxs-lookup"><span data-stu-id="48e53-114">Acquisition time.</span></span>

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

### <span data-ttu-id="48e53-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="48e53-115">-ExternalReferenceId</span></span>
<span data-ttu-id="48e53-116">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="48e53-116">External reference identifier.</span></span>

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

### <span data-ttu-id="48e53-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="48e53-117">-Id</span></span>
<span data-ttu-id="48e53-118">Azonosító a bérlői előfizetési környezetben</span><span class="sxs-lookup"><span data-stu-id="48e53-118">Identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="48e53-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="48e53-119">-PlanId</span></span>
<span data-ttu-id="48e53-120">Megtervezi az azonosítót a bérlői előfizetési környezetben.</span><span class="sxs-lookup"><span data-stu-id="48e53-120">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="48e53-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="48e53-121">-ProvisioningState</span></span>
<span data-ttu-id="48e53-122">A kiépítés állapota</span><span class="sxs-lookup"><span data-stu-id="48e53-122">State of the provisioning.</span></span>

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

### <span data-ttu-id="48e53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e53-123">CommonParameters</span></span>
<span data-ttu-id="48e53-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48e53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e53-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e53-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e53-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e53-126">INPUTS</span></span>

## <span data-ttu-id="48e53-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e53-127">OUTPUTS</span></span>

## <span data-ttu-id="48e53-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48e53-128">NOTES</span></span>

## <span data-ttu-id="48e53-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48e53-129">RELATED LINKS</span></span>

