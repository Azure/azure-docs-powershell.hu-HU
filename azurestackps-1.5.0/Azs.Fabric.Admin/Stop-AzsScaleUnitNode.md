---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491769"
---
# <span data-ttu-id="b8c13-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b8c13-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b8c13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8c13-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c13-103">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="b8c13-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="b8c13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8c13-104">SYNTAX</span></span>

### <span data-ttu-id="b8c13-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8c13-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c13-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c13-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c13-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8c13-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c13-108">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="b8c13-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="b8c13-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8c13-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c13-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8c13-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="b8c13-111">A Scale Unit csomópont leállítása</span><span class="sxs-lookup"><span data-stu-id="b8c13-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="b8c13-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8c13-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="b8c13-113">A Scale-egység csomópontjának kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="b8c13-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="b8c13-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8c13-114">PARAMETERS</span></span>

### <span data-ttu-id="b8c13-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8c13-115">-AsJob</span></span>
<span data-ttu-id="b8c13-116">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="b8c13-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b8c13-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c13-117">-Force</span></span>
<span data-ttu-id="b8c13-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8c13-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b8c13-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="b8c13-119">-Location</span></span>
<span data-ttu-id="b8c13-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b8c13-120">Location of the resource.</span></span>

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

### <span data-ttu-id="b8c13-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8c13-121">-Name</span></span>
<span data-ttu-id="b8c13-122">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="b8c13-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b8c13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c13-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8c13-124">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="b8c13-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b8c13-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c13-125">-ResourceId</span></span>
<span data-ttu-id="b8c13-126">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b8c13-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="b8c13-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="b8c13-127">-Shutdown</span></span>
<span data-ttu-id="b8c13-128">Ha a Scale egység csomópontot kecsesen leállítja, Ellenkező esetben Hard Power off a Scale Unit csomópontot.</span><span class="sxs-lookup"><span data-stu-id="b8c13-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="b8c13-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8c13-129">-Confirm</span></span>
<span data-ttu-id="b8c13-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8c13-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c13-131">-WhatIf</span></span>
<span data-ttu-id="b8c13-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8c13-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c13-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8c13-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c13-134">CommonParameters</span></span>
<span data-ttu-id="b8c13-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8c13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c13-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c13-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c13-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8c13-137">INPUTS</span></span>

## <span data-ttu-id="b8c13-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8c13-138">OUTPUTS</span></span>

## <span data-ttu-id="b8c13-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8c13-139">NOTES</span></span>

## <span data-ttu-id="b8c13-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8c13-140">RELATED LINKS</span></span>

