---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671756"
---
# <span data-ttu-id="c88e3-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="c88e3-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="c88e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c88e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c88e3-103">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c88e3-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="c88e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c88e3-104">SYNTAX</span></span>

### <span data-ttu-id="c88e3-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c88e3-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c88e3-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c88e3-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c88e3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c88e3-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c88e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c88e3-108">DESCRIPTION</span></span>
<span data-ttu-id="c88e3-109">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c88e3-109">Returns a list of each service's health.</span></span> <span data-ttu-id="c88e3-110">A AlertSummary tulajdonság a figyelmeztetés/hibák számát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c88e3-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="c88e3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c88e3-111">EXAMPLES</span></span>

### <span data-ttu-id="c88e3-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c88e3-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="c88e3-113">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c88e3-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="c88e3-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c88e3-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="c88e3-115">Egy szolgáltatás állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c88e3-115">Returns a service's health.</span></span>

## <span data-ttu-id="c88e3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c88e3-116">PARAMETERS</span></span>

### <span data-ttu-id="c88e3-117">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="c88e3-117">-Filter</span></span>
<span data-ttu-id="c88e3-118">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="c88e3-118">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e3-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="c88e3-119">-Location</span></span>
<span data-ttu-id="c88e3-120">A régió neve</span><span class="sxs-lookup"><span data-stu-id="c88e3-120">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e3-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c88e3-121">-Name</span></span>
<span data-ttu-id="c88e3-122">Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="c88e3-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="c88e3-124">Erőforráscsoport neve, amely az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="c88e3-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c88e3-125">-ResourceId</span></span>
<span data-ttu-id="c88e3-126">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c88e3-126">The resource id.</span></span>

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

### <span data-ttu-id="c88e3-127">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="c88e3-127">-Skip</span></span>
<span data-ttu-id="c88e3-128">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="c88e3-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c88e3-129">-Top</span><span class="sxs-lookup"><span data-stu-id="c88e3-129">-Top</span></span>
<span data-ttu-id="c88e3-130">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="c88e3-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c88e3-131">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="c88e3-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c88e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88e3-132">CommonParameters</span></span>
<span data-ttu-id="c88e3-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c88e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88e3-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c88e3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88e3-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c88e3-135">INPUTS</span></span>

## <span data-ttu-id="c88e3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c88e3-136">OUTPUTS</span></span>

### <span data-ttu-id="c88e3-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="c88e3-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="c88e3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c88e3-138">NOTES</span></span>

## <span data-ttu-id="c88e3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c88e3-139">RELATED LINKS</span></span>

