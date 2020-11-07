---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840509"
---
# <span data-ttu-id="ac43f-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="ac43f-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="ac43f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac43f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac43f-103">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="ac43f-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="ac43f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac43f-104">SYNTAX</span></span>

### <span data-ttu-id="ac43f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac43f-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ac43f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="ac43f-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="ac43f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac43f-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ac43f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac43f-108">DESCRIPTION</span></span>
<span data-ttu-id="ac43f-109">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="ac43f-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="ac43f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ac43f-110">EXAMPLES</span></span>

### <span data-ttu-id="ac43f-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ac43f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="ac43f-112">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="ac43f-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="ac43f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac43f-113">PARAMETERS</span></span>

### <span data-ttu-id="ac43f-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="ac43f-114">-AcquisitionId</span></span>
<span data-ttu-id="ac43f-115">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="ac43f-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43f-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac43f-116">-ResourceId</span></span>
<span data-ttu-id="ac43f-117">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ac43f-117">The resource id.</span></span>

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

### <span data-ttu-id="ac43f-118">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="ac43f-118">-Skip</span></span>
<span data-ttu-id="ac43f-119">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="ac43f-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ac43f-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac43f-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="ac43f-121">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="ac43f-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43f-122">-Top</span><span class="sxs-lookup"><span data-stu-id="ac43f-122">-Top</span></span>
<span data-ttu-id="ac43f-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="ac43f-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ac43f-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="ac43f-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ac43f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac43f-125">CommonParameters</span></span>
<span data-ttu-id="ac43f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac43f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac43f-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac43f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac43f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac43f-128">INPUTS</span></span>

## <span data-ttu-id="ac43f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac43f-129">OUTPUTS</span></span>

### <span data-ttu-id="ac43f-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="ac43f-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="ac43f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac43f-131">NOTES</span></span>

## <span data-ttu-id="ac43f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac43f-132">RELATED LINKS</span></span>

