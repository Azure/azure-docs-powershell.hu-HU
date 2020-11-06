---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d5870624b6d39b3e821ed6a7fb76d87c8422ab2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490827"
---
# <span data-ttu-id="b63c4-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b63c4-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b63c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b63c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b63c4-103">A hely összes méretarányos csomópontjának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b63c4-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="b63c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b63c4-104">SYNTAX</span></span>

### <span data-ttu-id="b63c4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b63c4-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b63c4-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b63c4-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b63c4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b63c4-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b63c4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b63c4-108">DESCRIPTION</span></span>
<span data-ttu-id="b63c4-109">A hely összes méretarányos csomópontjának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b63c4-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="b63c4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b63c4-110">EXAMPLES</span></span>

### <span data-ttu-id="b63c4-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b63c4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="b63c4-112">Az összes méretarányos csomópont lekérése egy helyen.</span><span class="sxs-lookup"><span data-stu-id="b63c4-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="b63c4-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b63c4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="b63c4-114">Egy adott méretarányú csomópontot kap egy olyan helyen, ahol nevet kapott.</span><span class="sxs-lookup"><span data-stu-id="b63c4-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="b63c4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b63c4-115">PARAMETERS</span></span>

### <span data-ttu-id="b63c4-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b63c4-116">-Filter</span></span>
<span data-ttu-id="b63c4-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b63c4-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b63c4-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="b63c4-118">-Location</span></span>
<span data-ttu-id="b63c4-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b63c4-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b63c4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b63c4-120">-Name</span></span>
<span data-ttu-id="b63c4-121">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="b63c4-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b63c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b63c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b63c4-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="b63c4-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b63c4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b63c4-124">-ResourceId</span></span>
<span data-ttu-id="b63c4-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b63c4-125">The resource id.</span></span>

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

### <span data-ttu-id="b63c4-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b63c4-126">-Skip</span></span>
<span data-ttu-id="b63c4-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b63c4-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b63c4-128">-Top</span><span class="sxs-lookup"><span data-stu-id="b63c4-128">-Top</span></span>
<span data-ttu-id="b63c4-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b63c4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b63c4-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b63c4-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b63c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63c4-131">CommonParameters</span></span>
<span data-ttu-id="b63c4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b63c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63c4-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b63c4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63c4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b63c4-134">INPUTS</span></span>

## <span data-ttu-id="b63c4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b63c4-135">OUTPUTS</span></span>

### <span data-ttu-id="b63c4-136">Microsoft. AzureStack. Management. Fabric. admin. models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b63c4-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="b63c4-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b63c4-137">NOTES</span></span>

## <span data-ttu-id="b63c4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b63c4-138">RELATED LINKS</span></span>

