---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840226"
---
# <span data-ttu-id="eb393-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="eb393-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="eb393-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb393-102">SYNOPSIS</span></span>
<span data-ttu-id="eb393-103">A méretarányos csomópont karbantartási módjának megkezdése</span><span class="sxs-lookup"><span data-stu-id="eb393-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eb393-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb393-104">SYNTAX</span></span>

### <span data-ttu-id="eb393-105">Letiltva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb393-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb393-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb393-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb393-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb393-107">DESCRIPTION</span></span>
<span data-ttu-id="eb393-108">A méretarányos csomópont karbantartási módjának megkezdése</span><span class="sxs-lookup"><span data-stu-id="eb393-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eb393-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eb393-109">EXAMPLES</span></span>

### <span data-ttu-id="eb393-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="eb393-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="eb393-111">Karbantartási mód engedélyezése egy méretarányos csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="eb393-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eb393-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb393-112">PARAMETERS</span></span>

### <span data-ttu-id="eb393-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb393-113">-Name</span></span>
<span data-ttu-id="eb393-114">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="eb393-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb393-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb393-115">-Location</span></span>
<span data-ttu-id="eb393-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eb393-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb393-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb393-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb393-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="eb393-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb393-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb393-119">-ResourceId</span></span>
<span data-ttu-id="eb393-120">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eb393-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="eb393-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb393-121">-AsJob</span></span>
<span data-ttu-id="eb393-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="eb393-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eb393-123">-Force</span><span class="sxs-lookup"><span data-stu-id="eb393-123">-Force</span></span>
<span data-ttu-id="eb393-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb393-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eb393-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb393-125">-WhatIf</span></span>
<span data-ttu-id="eb393-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb393-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb393-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb393-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb393-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb393-128">-Confirm</span></span>
<span data-ttu-id="eb393-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb393-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb393-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb393-130">CommonParameters</span></span>
<span data-ttu-id="eb393-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb393-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb393-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb393-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb393-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb393-133">INPUTS</span></span>

## <span data-ttu-id="eb393-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb393-134">OUTPUTS</span></span>

## <span data-ttu-id="eb393-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb393-135">NOTES</span></span>

## <span data-ttu-id="eb393-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb393-136">RELATED LINKS</span></span>
