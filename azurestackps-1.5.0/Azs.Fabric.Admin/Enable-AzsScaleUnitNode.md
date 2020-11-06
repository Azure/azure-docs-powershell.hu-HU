---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491075"
---
# <span data-ttu-id="4fd3f-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="4fd3f-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="4fd3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd3f-103">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="4fd3f-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4fd3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fd3f-104">SYNTAX</span></span>

### <span data-ttu-id="4fd3f-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fd3f-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd3f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd3f-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd3f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fd3f-107">DESCRIPTION</span></span>
<span data-ttu-id="4fd3f-108">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="4fd3f-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4fd3f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4fd3f-109">EXAMPLES</span></span>

### <span data-ttu-id="4fd3f-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4fd3f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="4fd3f-111">Állítsa le a karbantartási üzemmódot egy méretarányos csomóponton.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="4fd3f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fd3f-112">PARAMETERS</span></span>

### <span data-ttu-id="4fd3f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fd3f-113">-AsJob</span></span>
<span data-ttu-id="4fd3f-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4fd3f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4fd3f-115">-Force</span></span>
<span data-ttu-id="4fd3f-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4fd3f-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="4fd3f-117">-Location</span></span>
<span data-ttu-id="4fd3f-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-118">Location of the resource.</span></span>

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

### <span data-ttu-id="4fd3f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fd3f-119">-Name</span></span>
<span data-ttu-id="4fd3f-120">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="4fd3f-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="4fd3f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd3f-121">-ResourceGroupName</span></span>
<span data-ttu-id="4fd3f-122">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4fd3f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd3f-123">-ResourceId</span></span>
<span data-ttu-id="4fd3f-124">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4fd3f-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="4fd3f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fd3f-125">-Confirm</span></span>
<span data-ttu-id="4fd3f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd3f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd3f-127">-WhatIf</span></span>
<span data-ttu-id="4fd3f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd3f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd3f-130">CommonParameters</span></span>
<span data-ttu-id="4fd3f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fd3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd3f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd3f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd3f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fd3f-133">INPUTS</span></span>

## <span data-ttu-id="4fd3f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fd3f-134">OUTPUTS</span></span>

## <span data-ttu-id="4fd3f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fd3f-135">NOTES</span></span>

## <span data-ttu-id="4fd3f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fd3f-136">RELATED LINKS</span></span>

