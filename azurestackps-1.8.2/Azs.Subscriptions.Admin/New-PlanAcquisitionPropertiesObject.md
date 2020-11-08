---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016701"
---
# <span data-ttu-id="9570d-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="9570d-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="9570d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9570d-102">SYNOPSIS</span></span>
<span data-ttu-id="9570d-103">Az előfizetéshez tartozó bővítmény-terv megvásárlását jelöli.</span><span class="sxs-lookup"><span data-stu-id="9570d-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="9570d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9570d-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9570d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9570d-105">DESCRIPTION</span></span>
<span data-ttu-id="9570d-106">Az előfizetéshez tartozó bővítmény-terv megvásárlását jelöli.</span><span class="sxs-lookup"><span data-stu-id="9570d-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="9570d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9570d-107">EXAMPLES</span></span>

### <span data-ttu-id="9570d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9570d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9570d-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="9570d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9570d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9570d-110">PARAMETERS</span></span>

### <span data-ttu-id="9570d-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="9570d-111">-AcquisitionId</span></span>
<span data-ttu-id="9570d-112">A beszerzési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9570d-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="9570d-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="9570d-113">-AcquisitionTime</span></span>
<span data-ttu-id="9570d-114">Akvizíciós idő.</span><span class="sxs-lookup"><span data-stu-id="9570d-114">Acquisition time.</span></span>

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

### <span data-ttu-id="9570d-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="9570d-115">-ExternalReferenceId</span></span>
<span data-ttu-id="9570d-116">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="9570d-116">External reference identifier.</span></span>

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

### <span data-ttu-id="9570d-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9570d-117">-Id</span></span>
<span data-ttu-id="9570d-118">Azonosító a bérlői előfizetési környezetben</span><span class="sxs-lookup"><span data-stu-id="9570d-118">Identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="9570d-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="9570d-119">-PlanId</span></span>
<span data-ttu-id="9570d-120">Megtervezi az azonosítót a bérlői előfizetési környezetben.</span><span class="sxs-lookup"><span data-stu-id="9570d-120">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="9570d-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="9570d-121">-ProvisioningState</span></span>
<span data-ttu-id="9570d-122">A kiépítés állapota</span><span class="sxs-lookup"><span data-stu-id="9570d-122">State of the provisioning.</span></span>

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

### <span data-ttu-id="9570d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9570d-123">CommonParameters</span></span>
<span data-ttu-id="9570d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9570d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9570d-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9570d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9570d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9570d-126">INPUTS</span></span>

## <span data-ttu-id="9570d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9570d-127">OUTPUTS</span></span>

## <span data-ttu-id="9570d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9570d-128">NOTES</span></span>

## <span data-ttu-id="9570d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9570d-129">RELATED LINKS</span></span>

