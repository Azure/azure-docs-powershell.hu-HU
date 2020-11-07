---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840272"
---
# <span data-ttu-id="db1fe-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="db1fe-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="db1fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="db1fe-103">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="db1fe-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="db1fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db1fe-104">SYNTAX</span></span>

### <span data-ttu-id="db1fe-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db1fe-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="db1fe-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="db1fe-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="db1fe-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="db1fe-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="db1fe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="db1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="db1fe-109">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="db1fe-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="db1fe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="db1fe-110">EXAMPLES</span></span>

### <span data-ttu-id="db1fe-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="db1fe-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="db1fe-112">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="db1fe-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="db1fe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db1fe-113">PARAMETERS</span></span>

### <span data-ttu-id="db1fe-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="db1fe-114">-Location</span></span>
<span data-ttu-id="db1fe-115">A régió neve</span><span class="sxs-lookup"><span data-stu-id="db1fe-115">Name of the region</span></span>

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

### <span data-ttu-id="db1fe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1fe-116">-ResourceGroupName</span></span>
<span data-ttu-id="db1fe-117">Erőforráscsoport neve, nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="db1fe-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="db1fe-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db1fe-118">-ResourceId</span></span>
<span data-ttu-id="db1fe-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="db1fe-119">The resource id.</span></span>

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

### <span data-ttu-id="db1fe-120">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="db1fe-120">-Filter</span></span>
<span data-ttu-id="db1fe-121">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="db1fe-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="db1fe-122">-Top</span><span class="sxs-lookup"><span data-stu-id="db1fe-122">-Top</span></span>
<span data-ttu-id="db1fe-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="db1fe-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="db1fe-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="db1fe-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="db1fe-125">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="db1fe-125">-Skip</span></span>
<span data-ttu-id="db1fe-126">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="db1fe-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="db1fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1fe-127">CommonParameters</span></span>
<span data-ttu-id="db1fe-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db1fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1fe-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1fe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1fe-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db1fe-130">INPUTS</span></span>

## <span data-ttu-id="db1fe-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db1fe-131">OUTPUTS</span></span>

### <span data-ttu-id="db1fe-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="db1fe-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="db1fe-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db1fe-133">NOTES</span></span>

## <span data-ttu-id="db1fe-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db1fe-134">RELATED LINKS</span></span>
