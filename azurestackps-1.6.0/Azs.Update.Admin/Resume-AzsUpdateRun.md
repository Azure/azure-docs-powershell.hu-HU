---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671768"
---
# <span data-ttu-id="4d803-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4d803-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="4d803-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d803-102">SYNOPSIS</span></span>
<span data-ttu-id="4d803-103">Folytatja a korábban megkezdett frissítési futtatást, amely sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="4d803-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="4d803-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d803-104">SYNTAX</span></span>

### <span data-ttu-id="4d803-105">UpdateRuns_Rerun (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d803-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d803-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d803-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d803-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d803-107">DESCRIPTION</span></span>
<span data-ttu-id="4d803-108">Folytatja a korábban megkezdett frissítési futtatást, amely sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="4d803-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="4d803-109">Az újraindítást követően futtatott frissítés folytatódik abban a pontban, amikor az utolsó sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="4d803-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="4d803-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4d803-110">EXAMPLES</span></span>

### <span data-ttu-id="4d803-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d803-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="4d803-112">Folytatja a korábban megkezdett frissítési futtatást, amely sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="4d803-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="4d803-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d803-113">PARAMETERS</span></span>

### <span data-ttu-id="4d803-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d803-114">-AsJob</span></span>
<span data-ttu-id="4d803-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="4d803-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4d803-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4d803-116">-Force</span></span>
<span data-ttu-id="4d803-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d803-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4d803-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="4d803-118">-Location</span></span>
<span data-ttu-id="4d803-119">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="4d803-119">The name of the update location.</span></span>

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

### <span data-ttu-id="4d803-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d803-120">-Name</span></span>
<span data-ttu-id="4d803-121">A futtatási azonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="4d803-121">Update run identifier.</span></span>

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

### <span data-ttu-id="4d803-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d803-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d803-123">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="4d803-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4d803-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d803-124">-ResourceId</span></span>
<span data-ttu-id="4d803-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4d803-125">The resource id.</span></span>

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

### <span data-ttu-id="4d803-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="4d803-126">-UpdateName</span></span>
<span data-ttu-id="4d803-127">A frissítés megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="4d803-127">Display name of the update.</span></span>

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

### <span data-ttu-id="4d803-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d803-128">-Confirm</span></span>
<span data-ttu-id="4d803-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d803-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d803-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d803-130">-WhatIf</span></span>
<span data-ttu-id="4d803-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d803-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d803-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d803-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d803-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d803-133">CommonParameters</span></span>
<span data-ttu-id="4d803-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d803-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d803-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d803-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d803-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d803-136">INPUTS</span></span>

## <span data-ttu-id="4d803-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d803-137">OUTPUTS</span></span>

## <span data-ttu-id="4d803-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d803-138">NOTES</span></span>

## <span data-ttu-id="4d803-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d803-139">RELATED LINKS</span></span>

