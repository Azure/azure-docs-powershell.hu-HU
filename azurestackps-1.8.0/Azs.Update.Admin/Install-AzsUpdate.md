---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840135"
---
# <span data-ttu-id="3ff00-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="3ff00-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="3ff00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ff00-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff00-103">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="3ff00-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="3ff00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ff00-104">SYNTAX</span></span>

### <span data-ttu-id="3ff00-105">Apply (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ff00-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff00-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff00-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff00-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ff00-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff00-108">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="3ff00-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="3ff00-109">A felkérést követően Get-AzsUpdateRun a frissítés folyamatának módosítására is használhatók.</span><span class="sxs-lookup"><span data-stu-id="3ff00-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="3ff00-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ff00-110">EXAMPLES</span></span>

### <span data-ttu-id="3ff00-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="3ff00-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="3ff00-112">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="3ff00-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="3ff00-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ff00-113">PARAMETERS</span></span>

### <span data-ttu-id="3ff00-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ff00-114">-Name</span></span>
<span data-ttu-id="3ff00-115">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="3ff00-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff00-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff00-116">-ResourceGroupName</span></span>
<span data-ttu-id="3ff00-117">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="3ff00-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff00-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="3ff00-118">-Location</span></span>
<span data-ttu-id="3ff00-119">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="3ff00-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff00-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ff00-120">-AsJob</span></span>
<span data-ttu-id="3ff00-121">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="3ff00-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3ff00-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff00-122">-ResourceId</span></span>
<span data-ttu-id="3ff00-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3ff00-123">The resource id.</span></span>

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

### <span data-ttu-id="3ff00-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3ff00-124">-Force</span></span>
<span data-ttu-id="3ff00-125">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="3ff00-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="3ff00-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff00-126">-WhatIf</span></span>
<span data-ttu-id="3ff00-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ff00-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff00-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ff00-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff00-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ff00-129">-Confirm</span></span>
<span data-ttu-id="3ff00-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ff00-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff00-131">CommonParameters</span></span>
<span data-ttu-id="3ff00-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ff00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff00-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff00-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff00-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff00-134">INPUTS</span></span>

## <span data-ttu-id="3ff00-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff00-135">OUTPUTS</span></span>

### <span data-ttu-id="3ff00-136">Microsoft. AzureStack. Management. Update. admin. modellek. Update</span><span class="sxs-lookup"><span data-stu-id="3ff00-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="3ff00-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ff00-137">NOTES</span></span>

## <span data-ttu-id="3ff00-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ff00-138">RELATED LINKS</span></span>
