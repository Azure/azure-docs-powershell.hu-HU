---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491127"
---
# <span data-ttu-id="55b3b-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="55b3b-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="55b3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="55b3b-103">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="55b3b-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="55b3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55b3b-104">SYNTAX</span></span>

### <span data-ttu-id="55b3b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55b3b-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="55b3b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="55b3b-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="55b3b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="55b3b-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="55b3b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="55b3b-108">DESCRIPTION</span></span>
<span data-ttu-id="55b3b-109">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="55b3b-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="55b3b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="55b3b-110">EXAMPLES</span></span>

### <span data-ttu-id="55b3b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="55b3b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="55b3b-112">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="55b3b-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="55b3b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55b3b-113">PARAMETERS</span></span>

### <span data-ttu-id="55b3b-114">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="55b3b-114">-Filter</span></span>
<span data-ttu-id="55b3b-115">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="55b3b-115">OData filter parameter.</span></span>

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

### <span data-ttu-id="55b3b-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="55b3b-116">-Location</span></span>
<span data-ttu-id="55b3b-117">A régió neve</span><span class="sxs-lookup"><span data-stu-id="55b3b-117">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55b3b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b3b-118">-ResourceGroupName</span></span>
<span data-ttu-id="55b3b-119">Erőforráscsoport neve, amely az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="55b3b-119">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="55b3b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55b3b-120">-ResourceId</span></span>
<span data-ttu-id="55b3b-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="55b3b-121">The resource id.</span></span>

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

### <span data-ttu-id="55b3b-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="55b3b-122">-Skip</span></span>
<span data-ttu-id="55b3b-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="55b3b-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="55b3b-124">-Top</span><span class="sxs-lookup"><span data-stu-id="55b3b-124">-Top</span></span>
<span data-ttu-id="55b3b-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="55b3b-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="55b3b-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="55b3b-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="55b3b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b3b-127">CommonParameters</span></span>
<span data-ttu-id="55b3b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55b3b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b3b-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b3b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b3b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55b3b-130">INPUTS</span></span>

## <span data-ttu-id="55b3b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55b3b-131">OUTPUTS</span></span>

### <span data-ttu-id="55b3b-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="55b3b-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="55b3b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55b3b-133">NOTES</span></span>

## <span data-ttu-id="55b3b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55b3b-134">RELATED LINKS</span></span>

