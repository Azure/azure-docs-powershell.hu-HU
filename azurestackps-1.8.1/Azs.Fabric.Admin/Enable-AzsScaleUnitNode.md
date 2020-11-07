---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840909"
---
# <span data-ttu-id="d32fe-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d32fe-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d32fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d32fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d32fe-103">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="d32fe-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d32fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d32fe-104">SYNTAX</span></span>

### <span data-ttu-id="d32fe-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d32fe-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d32fe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d32fe-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d32fe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d32fe-107">DESCRIPTION</span></span>
<span data-ttu-id="d32fe-108">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="d32fe-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d32fe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d32fe-109">EXAMPLES</span></span>

### <span data-ttu-id="d32fe-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="d32fe-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="d32fe-111">Állítsa le a karbantartási üzemmódot egy méretarányos csomóponton.</span><span class="sxs-lookup"><span data-stu-id="d32fe-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="d32fe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d32fe-112">PARAMETERS</span></span>

### <span data-ttu-id="d32fe-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d32fe-113">-Name</span></span>
<span data-ttu-id="d32fe-114">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="d32fe-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32fe-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="d32fe-115">-Location</span></span>
<span data-ttu-id="d32fe-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d32fe-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d32fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="d32fe-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="d32fe-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32fe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d32fe-119">-ResourceId</span></span>
<span data-ttu-id="d32fe-120">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d32fe-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="d32fe-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d32fe-121">-AsJob</span></span>
<span data-ttu-id="d32fe-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="d32fe-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d32fe-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d32fe-123">-Force</span></span>
<span data-ttu-id="d32fe-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d32fe-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d32fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d32fe-125">-WhatIf</span></span>
<span data-ttu-id="d32fe-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d32fe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d32fe-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d32fe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d32fe-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d32fe-128">-Confirm</span></span>
<span data-ttu-id="d32fe-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d32fe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d32fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32fe-130">CommonParameters</span></span>
<span data-ttu-id="d32fe-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d32fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32fe-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d32fe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32fe-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d32fe-133">INPUTS</span></span>

## <span data-ttu-id="d32fe-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d32fe-134">OUTPUTS</span></span>

## <span data-ttu-id="d32fe-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d32fe-135">NOTES</span></span>

## <span data-ttu-id="d32fe-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d32fe-136">RELATED LINKS</span></span>
