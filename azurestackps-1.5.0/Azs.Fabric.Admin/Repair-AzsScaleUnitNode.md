---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490896"
---
# <span data-ttu-id="e76b9-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e76b9-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e76b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e76b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e76b9-103">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="e76b9-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="e76b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e76b9-104">SYNTAX</span></span>

### <span data-ttu-id="e76b9-105">Javítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e76b9-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e76b9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e76b9-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e76b9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e76b9-107">DESCRIPTION</span></span>
<span data-ttu-id="e76b9-108">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="e76b9-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="e76b9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e76b9-109">EXAMPLES</span></span>

### <span data-ttu-id="e76b9-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e76b9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="e76b9-111">A Scale Unit csomópont kijavítása.</span><span class="sxs-lookup"><span data-stu-id="e76b9-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="e76b9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e76b9-112">PARAMETERS</span></span>

### <span data-ttu-id="e76b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e76b9-113">-AsJob</span></span>
<span data-ttu-id="e76b9-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="e76b9-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e76b9-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="e76b9-115">-BMCIPv4Address</span></span>
<span data-ttu-id="e76b9-116">A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="e76b9-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="e76b9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e76b9-117">-Force</span></span>
<span data-ttu-id="e76b9-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e76b9-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e76b9-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="e76b9-119">-Location</span></span>
<span data-ttu-id="e76b9-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e76b9-120">Location of the resource.</span></span>

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

### <span data-ttu-id="e76b9-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e76b9-121">-Name</span></span>
<span data-ttu-id="e76b9-122">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="e76b9-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="e76b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e76b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e76b9-124">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="e76b9-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e76b9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e76b9-125">-ResourceId</span></span>
<span data-ttu-id="e76b9-126">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e76b9-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e76b9-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e76b9-127">-Confirm</span></span>
<span data-ttu-id="e76b9-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e76b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e76b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76b9-129">-WhatIf</span></span>
<span data-ttu-id="e76b9-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e76b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76b9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e76b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e76b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76b9-132">CommonParameters</span></span>
<span data-ttu-id="e76b9-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e76b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76b9-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e76b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76b9-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e76b9-135">INPUTS</span></span>

## <span data-ttu-id="e76b9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e76b9-136">OUTPUTS</span></span>

## <span data-ttu-id="e76b9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e76b9-137">NOTES</span></span>

## <span data-ttu-id="e76b9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e76b9-138">RELATED LINKS</span></span>

