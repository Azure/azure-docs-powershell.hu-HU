---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840183"
---
# <span data-ttu-id="f4452-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f4452-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f4452-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4452-102">SYNOPSIS</span></span>
<span data-ttu-id="f4452-103">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="f4452-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="f4452-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4452-104">SYNTAX</span></span>

### <span data-ttu-id="f4452-105">Javítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4452-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4452-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4452-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4452-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4452-107">DESCRIPTION</span></span>
<span data-ttu-id="f4452-108">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="f4452-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="f4452-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f4452-109">EXAMPLES</span></span>

### <span data-ttu-id="f4452-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="f4452-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="f4452-111">A Scale Unit csomópont kijavítása.</span><span class="sxs-lookup"><span data-stu-id="f4452-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="f4452-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4452-112">PARAMETERS</span></span>

### <span data-ttu-id="f4452-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4452-113">-Name</span></span>
<span data-ttu-id="f4452-114">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="f4452-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4452-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="f4452-115">-BMCIPv4Address</span></span>
<span data-ttu-id="f4452-116">A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="f4452-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4452-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="f4452-117">-Location</span></span>
<span data-ttu-id="f4452-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f4452-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4452-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4452-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4452-120">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="f4452-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4452-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4452-121">-ResourceId</span></span>
<span data-ttu-id="f4452-122">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f4452-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="f4452-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4452-123">-AsJob</span></span>
<span data-ttu-id="f4452-124">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="f4452-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f4452-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f4452-125">-Force</span></span>
<span data-ttu-id="f4452-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4452-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f4452-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4452-127">-WhatIf</span></span>
<span data-ttu-id="f4452-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4452-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4452-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4452-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4452-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4452-130">-Confirm</span></span>
<span data-ttu-id="f4452-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4452-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4452-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4452-132">CommonParameters</span></span>
<span data-ttu-id="f4452-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4452-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4452-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4452-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4452-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4452-135">INPUTS</span></span>

## <span data-ttu-id="f4452-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4452-136">OUTPUTS</span></span>

## <span data-ttu-id="f4452-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4452-137">NOTES</span></span>

## <span data-ttu-id="f4452-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4452-138">RELATED LINKS</span></span>
