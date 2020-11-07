---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839827"
---
# <span data-ttu-id="be500-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="be500-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="be500-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be500-102">SYNOPSIS</span></span>
<span data-ttu-id="be500-103">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="be500-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="be500-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be500-104">SYNTAX</span></span>

### <span data-ttu-id="be500-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be500-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="be500-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="be500-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="be500-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="be500-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="be500-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="be500-108">DESCRIPTION</span></span>
<span data-ttu-id="be500-109">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="be500-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="be500-110">Példák</span><span class="sxs-lookup"><span data-stu-id="be500-110">EXAMPLES</span></span>

### <span data-ttu-id="be500-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="be500-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="be500-112">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="be500-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="be500-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be500-113">PARAMETERS</span></span>

### <span data-ttu-id="be500-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="be500-114">-AcquisitionId</span></span>
<span data-ttu-id="be500-115">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="be500-115">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="be500-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be500-116">-ResourceId</span></span>
<span data-ttu-id="be500-117">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="be500-117">The resource id.</span></span>

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

### <span data-ttu-id="be500-118">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="be500-118">-Skip</span></span>
<span data-ttu-id="be500-119">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="be500-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="be500-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be500-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="be500-121">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="be500-121">The target subscription ID.</span></span>

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

### <span data-ttu-id="be500-122">-Top</span><span class="sxs-lookup"><span data-stu-id="be500-122">-Top</span></span>
<span data-ttu-id="be500-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="be500-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="be500-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="be500-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="be500-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be500-125">CommonParameters</span></span>
<span data-ttu-id="be500-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be500-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be500-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be500-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be500-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be500-128">INPUTS</span></span>

## <span data-ttu-id="be500-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be500-129">OUTPUTS</span></span>

### <span data-ttu-id="be500-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="be500-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="be500-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be500-131">NOTES</span></span>

## <span data-ttu-id="be500-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be500-132">RELATED LINKS</span></span>

