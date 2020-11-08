---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016649"
---
# <span data-ttu-id="eade4-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="eade4-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="eade4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eade4-102">SYNOPSIS</span></span>
<span data-ttu-id="eade4-103">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="eade4-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eade4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eade4-104">SYNTAX</span></span>

### <span data-ttu-id="eade4-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eade4-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eade4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eade4-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eade4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eade4-107">DESCRIPTION</span></span>
<span data-ttu-id="eade4-108">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="eade4-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eade4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eade4-109">EXAMPLES</span></span>

### <span data-ttu-id="eade4-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="eade4-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="eade4-111">Állítsa le a karbantartási üzemmódot egy méretarányos csomóponton.</span><span class="sxs-lookup"><span data-stu-id="eade4-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="eade4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eade4-112">PARAMETERS</span></span>

### <span data-ttu-id="eade4-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eade4-113">-Name</span></span>
<span data-ttu-id="eade4-114">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="eade4-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="eade4-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="eade4-115">-Location</span></span>
<span data-ttu-id="eade4-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eade4-116">Location of the resource.</span></span>

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

### <span data-ttu-id="eade4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eade4-117">-ResourceGroupName</span></span>
<span data-ttu-id="eade4-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="eade4-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eade4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eade4-119">-ResourceId</span></span>
<span data-ttu-id="eade4-120">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eade4-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="eade4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eade4-121">-AsJob</span></span>
<span data-ttu-id="eade4-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="eade4-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eade4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="eade4-123">-Force</span></span>
<span data-ttu-id="eade4-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eade4-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eade4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eade4-125">-WhatIf</span></span>
<span data-ttu-id="eade4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eade4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eade4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eade4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eade4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eade4-128">-Confirm</span></span>
<span data-ttu-id="eade4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eade4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eade4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eade4-130">CommonParameters</span></span>
<span data-ttu-id="eade4-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eade4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eade4-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eade4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eade4-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eade4-133">INPUTS</span></span>

## <span data-ttu-id="eade4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eade4-134">OUTPUTS</span></span>

## <span data-ttu-id="eade4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eade4-135">NOTES</span></span>

## <span data-ttu-id="eade4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eade4-136">RELATED LINKS</span></span>
