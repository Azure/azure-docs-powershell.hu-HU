---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70ee408b65839e46e408256780a6d705c9881bde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490724"
---
# <span data-ttu-id="653dc-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="653dc-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="653dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="653dc-102">SYNOPSIS</span></span>
<span data-ttu-id="653dc-103">A méretarányos csomópont karbantartási módjának megkezdése</span><span class="sxs-lookup"><span data-stu-id="653dc-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="653dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="653dc-104">SYNTAX</span></span>

### <span data-ttu-id="653dc-105">Letiltva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="653dc-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="653dc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="653dc-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="653dc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="653dc-107">DESCRIPTION</span></span>
<span data-ttu-id="653dc-108">A méretarányos csomópont karbantartási módjának megkezdése</span><span class="sxs-lookup"><span data-stu-id="653dc-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="653dc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="653dc-109">EXAMPLES</span></span>

### <span data-ttu-id="653dc-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="653dc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="653dc-111">Karbantartási mód engedélyezése egy méretarányos csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="653dc-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="653dc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="653dc-112">PARAMETERS</span></span>

### <span data-ttu-id="653dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="653dc-113">-AsJob</span></span>
<span data-ttu-id="653dc-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="653dc-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="653dc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="653dc-115">-Force</span></span>
<span data-ttu-id="653dc-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="653dc-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="653dc-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="653dc-117">-Location</span></span>
<span data-ttu-id="653dc-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="653dc-118">Location of the resource.</span></span>

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

### <span data-ttu-id="653dc-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="653dc-119">-Name</span></span>
<span data-ttu-id="653dc-120">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="653dc-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="653dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="653dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="653dc-122">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="653dc-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="653dc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="653dc-123">-ResourceId</span></span>
<span data-ttu-id="653dc-124">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="653dc-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="653dc-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="653dc-125">-Confirm</span></span>
<span data-ttu-id="653dc-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="653dc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="653dc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="653dc-127">-WhatIf</span></span>
<span data-ttu-id="653dc-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="653dc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="653dc-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="653dc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="653dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653dc-130">CommonParameters</span></span>
<span data-ttu-id="653dc-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="653dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653dc-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="653dc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653dc-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="653dc-133">INPUTS</span></span>

## <span data-ttu-id="653dc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="653dc-134">OUTPUTS</span></span>

## <span data-ttu-id="653dc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="653dc-135">NOTES</span></span>

## <span data-ttu-id="653dc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="653dc-136">RELATED LINKS</span></span>

