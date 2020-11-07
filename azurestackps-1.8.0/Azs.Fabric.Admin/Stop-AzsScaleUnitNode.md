---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840291"
---
# <span data-ttu-id="8c0ed-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8c0ed-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8c0ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0ed-103">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="8c0ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c0ed-104">SYNTAX</span></span>

### <span data-ttu-id="8c0ed-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c0ed-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0ed-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0ed-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c0ed-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c0ed-107">DESCRIPTION</span></span>
<span data-ttu-id="8c0ed-108">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="8c0ed-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c0ed-109">EXAMPLES</span></span>

### <span data-ttu-id="8c0ed-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="8c0ed-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="8c0ed-111">A Scale Unit csomópont leállítása</span><span class="sxs-lookup"><span data-stu-id="8c0ed-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="8c0ed-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="8c0ed-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="8c0ed-113">A Scale-egység csomópontjának kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="8c0ed-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c0ed-114">PARAMETERS</span></span>

### <span data-ttu-id="8c0ed-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c0ed-115">-Name</span></span>
<span data-ttu-id="8c0ed-116">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="8c0ed-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0ed-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="8c0ed-117">-Location</span></span>
<span data-ttu-id="8c0ed-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c0ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c0ed-120">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0ed-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0ed-121">-ResourceId</span></span>
<span data-ttu-id="8c0ed-122">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8c0ed-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="8c0ed-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="8c0ed-123">-Shutdown</span></span>
<span data-ttu-id="8c0ed-124">Ha a Scale egység csomópontot kecsesen leállítja, Ellenkező esetben Hard Power off a Scale Unit csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="8c0ed-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c0ed-125">-AsJob</span></span>
<span data-ttu-id="8c0ed-126">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8c0ed-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8c0ed-127">-Force</span></span>
<span data-ttu-id="8c0ed-128">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8c0ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0ed-129">-WhatIf</span></span>
<span data-ttu-id="8c0ed-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0ed-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0ed-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c0ed-132">-Confirm</span></span>
<span data-ttu-id="8c0ed-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0ed-134">CommonParameters</span></span>
<span data-ttu-id="8c0ed-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c0ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0ed-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c0ed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0ed-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c0ed-137">INPUTS</span></span>

## <span data-ttu-id="8c0ed-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c0ed-138">OUTPUTS</span></span>

## <span data-ttu-id="8c0ed-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c0ed-139">NOTES</span></span>

## <span data-ttu-id="8c0ed-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c0ed-140">RELATED LINKS</span></span>
