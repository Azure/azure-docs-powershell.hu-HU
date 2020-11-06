---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491588"
---
# <span data-ttu-id="049ef-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="049ef-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="049ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="049ef-102">SYNOPSIS</span></span>
<span data-ttu-id="049ef-103">A helyhez tartozó összes méretarány listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="049ef-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="049ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="049ef-104">SYNTAX</span></span>

### <span data-ttu-id="049ef-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="049ef-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="049ef-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="049ef-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="049ef-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="049ef-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="049ef-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="049ef-108">DESCRIPTION</span></span>
<span data-ttu-id="049ef-109">A helyhez tartozó összes méretarány listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="049ef-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="049ef-110">Példák</span><span class="sxs-lookup"><span data-stu-id="049ef-110">EXAMPLES</span></span>

### <span data-ttu-id="049ef-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="049ef-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="049ef-112">A méretarányokat tartalmazó adatok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="049ef-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="049ef-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="049ef-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="049ef-114">Adott méretarányú egység adatainak visszaadása.</span><span class="sxs-lookup"><span data-stu-id="049ef-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="049ef-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="049ef-115">PARAMETERS</span></span>

### <span data-ttu-id="049ef-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="049ef-116">-Filter</span></span>
<span data-ttu-id="049ef-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="049ef-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="049ef-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="049ef-118">-Location</span></span>
<span data-ttu-id="049ef-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="049ef-119">Location of the resource.</span></span>

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

### <span data-ttu-id="049ef-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="049ef-120">-Name</span></span>
<span data-ttu-id="049ef-121">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="049ef-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="049ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="049ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="049ef-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="049ef-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="049ef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="049ef-124">-ResourceId</span></span>
<span data-ttu-id="049ef-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="049ef-125">The resource id.</span></span>

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

### <span data-ttu-id="049ef-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="049ef-126">-Skip</span></span>
<span data-ttu-id="049ef-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="049ef-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="049ef-128">-Top</span><span class="sxs-lookup"><span data-stu-id="049ef-128">-Top</span></span>
<span data-ttu-id="049ef-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="049ef-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="049ef-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="049ef-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="049ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049ef-131">CommonParameters</span></span>
<span data-ttu-id="049ef-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="049ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049ef-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="049ef-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049ef-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="049ef-134">INPUTS</span></span>

## <span data-ttu-id="049ef-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="049ef-135">OUTPUTS</span></span>

### <span data-ttu-id="049ef-136">Microsoft. AzureStack. Management. Fabric. admin. models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="049ef-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="049ef-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="049ef-137">NOTES</span></span>

## <span data-ttu-id="049ef-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="049ef-138">RELATED LINKS</span></span>

