---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017064"
---
# <span data-ttu-id="41ea3-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="41ea3-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="41ea3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="41ea3-103">Folytatja a korábban megkezdett frissítési futtatást, amely sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="41ea3-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="41ea3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41ea3-104">SYNTAX</span></span>

### <span data-ttu-id="41ea3-105">UpdateRuns_Rerun (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41ea3-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ea3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41ea3-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41ea3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41ea3-107">DESCRIPTION</span></span>
<span data-ttu-id="41ea3-108">Folytatja a korábban megkezdett frissítési futtatást, amely sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="41ea3-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="41ea3-109">Az újraindítást követően futtatott frissítés folytatódik abban a pontban, amikor az utolsó sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="41ea3-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="41ea3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="41ea3-110">EXAMPLES</span></span>

### <span data-ttu-id="41ea3-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="41ea3-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="41ea3-112">Folytatja a korábban megkezdett frissítési futtatást, amely sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="41ea3-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="41ea3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41ea3-113">PARAMETERS</span></span>

### <span data-ttu-id="41ea3-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41ea3-114">-Name</span></span>
<span data-ttu-id="41ea3-115">A futtatási azonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="41ea3-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea3-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="41ea3-116">-Location</span></span>
<span data-ttu-id="41ea3-117">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="41ea3-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ea3-118">-ResourceGroupName</span></span>
<span data-ttu-id="41ea3-119">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="41ea3-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea3-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="41ea3-120">-UpdateName</span></span>
<span data-ttu-id="41ea3-121">A frissítés megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="41ea3-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ea3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41ea3-122">-AsJob</span></span>
<span data-ttu-id="41ea3-123">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="41ea3-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="41ea3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41ea3-124">-ResourceId</span></span>
<span data-ttu-id="41ea3-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="41ea3-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41ea3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="41ea3-126">-Force</span></span>
<span data-ttu-id="41ea3-127">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="41ea3-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="41ea3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ea3-128">-WhatIf</span></span>
<span data-ttu-id="41ea3-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41ea3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41ea3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41ea3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41ea3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41ea3-131">-Confirm</span></span>
<span data-ttu-id="41ea3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41ea3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41ea3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ea3-133">CommonParameters</span></span>
<span data-ttu-id="41ea3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41ea3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ea3-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ea3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ea3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ea3-136">INPUTS</span></span>

## <span data-ttu-id="41ea3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ea3-137">OUTPUTS</span></span>

## <span data-ttu-id="41ea3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41ea3-138">NOTES</span></span>

## <span data-ttu-id="41ea3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41ea3-139">RELATED LINKS</span></span>
