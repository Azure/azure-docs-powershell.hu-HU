---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491399"
---
# <span data-ttu-id="85455-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="85455-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="85455-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85455-102">SYNOPSIS</span></span>
<span data-ttu-id="85455-103">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="85455-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="85455-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85455-104">SYNTAX</span></span>

### <span data-ttu-id="85455-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85455-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85455-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="85455-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85455-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="85455-107">DESCRIPTION</span></span>
<span data-ttu-id="85455-108">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="85455-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="85455-109">Példák</span><span class="sxs-lookup"><span data-stu-id="85455-109">EXAMPLES</span></span>

### <span data-ttu-id="85455-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85455-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="85455-111">ProvisioningState: sikerült</span><span class="sxs-lookup"><span data-stu-id="85455-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="85455-112">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="85455-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="85455-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85455-113">PARAMETERS</span></span>

### <span data-ttu-id="85455-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85455-114">-AsJob</span></span>
<span data-ttu-id="85455-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="85455-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="85455-116">-Force</span><span class="sxs-lookup"><span data-stu-id="85455-116">-Force</span></span>
<span data-ttu-id="85455-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85455-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="85455-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="85455-118">-Location</span></span>
<span data-ttu-id="85455-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="85455-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85455-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="85455-120">-Name</span></span>
<span data-ttu-id="85455-121">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="85455-121">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85455-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85455-122">-ResourceGroupName</span></span>
<span data-ttu-id="85455-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="85455-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85455-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85455-124">-ResourceId</span></span>
<span data-ttu-id="85455-125">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="85455-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="85455-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="85455-126">-Confirm</span></span>
<span data-ttu-id="85455-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85455-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85455-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85455-128">-WhatIf</span></span>
<span data-ttu-id="85455-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="85455-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85455-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85455-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85455-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85455-131">CommonParameters</span></span>
<span data-ttu-id="85455-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85455-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85455-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85455-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85455-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85455-134">INPUTS</span></span>

## <span data-ttu-id="85455-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85455-135">OUTPUTS</span></span>

## <span data-ttu-id="85455-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85455-136">NOTES</span></span>

## <span data-ttu-id="85455-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85455-137">RELATED LINKS</span></span>

