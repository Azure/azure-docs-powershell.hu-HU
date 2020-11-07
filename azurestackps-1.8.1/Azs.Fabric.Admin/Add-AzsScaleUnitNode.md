---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840910"
---
# <span data-ttu-id="af350-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="af350-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="af350-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af350-102">SYNOPSIS</span></span>
<span data-ttu-id="af350-103">Új léptékű egység hozzáadása</span><span class="sxs-lookup"><span data-stu-id="af350-103">Add a new scale unit.</span></span>

## <span data-ttu-id="af350-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af350-104">SYNTAX</span></span>

### <span data-ttu-id="af350-105">ScaleOut (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af350-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af350-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af350-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af350-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af350-107">DESCRIPTION</span></span>
<span data-ttu-id="af350-108">Új léptékű egység hozzáadása</span><span class="sxs-lookup"><span data-stu-id="af350-108">Add a new scale unit.</span></span>

## <span data-ttu-id="af350-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af350-109">EXAMPLES</span></span>

### <span data-ttu-id="af350-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="af350-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="af350-111">Hozzon létre egy új méretarányos csomópontot.</span><span class="sxs-lookup"><span data-stu-id="af350-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="af350-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af350-112">PARAMETERS</span></span>

### <span data-ttu-id="af350-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af350-113">-AsJob</span></span>
<span data-ttu-id="af350-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="af350-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="af350-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="af350-116">A jelölő jelzi, ha a műveletnek a tárterületre várnia kell, hogy ne térjen vissza az eredményre.</span><span class="sxs-lookup"><span data-stu-id="af350-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-117">-Force</span><span class="sxs-lookup"><span data-stu-id="af350-117">-Force</span></span>
<span data-ttu-id="af350-118">Nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="af350-118">Don't ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="af350-119">-Location</span></span>
<span data-ttu-id="af350-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="af350-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af350-121">-Name</span></span>
<span data-ttu-id="af350-122">{{Kitöltés név leírása}}</span><span class="sxs-lookup"><span data-stu-id="af350-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="af350-123">-NodeList</span></span>
<span data-ttu-id="af350-124">Csomópontok listája a méretarányt tartalmazó egységben.</span><span class="sxs-lookup"><span data-stu-id="af350-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af350-125">-ResourceGroupName</span></span>
<span data-ttu-id="af350-126">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="af350-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af350-127">-ResourceId</span></span>
<span data-ttu-id="af350-128">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="af350-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="af350-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af350-129">-Confirm</span></span>
<span data-ttu-id="af350-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af350-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af350-131">-WhatIf</span></span>
<span data-ttu-id="af350-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af350-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af350-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af350-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af350-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af350-134">CommonParameters</span></span>
<span data-ttu-id="af350-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af350-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af350-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af350-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af350-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af350-137">INPUTS</span></span>

## <span data-ttu-id="af350-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af350-138">OUTPUTS</span></span>

## <span data-ttu-id="af350-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af350-139">NOTES</span></span>

## <span data-ttu-id="af350-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af350-140">RELATED LINKS</span></span>

