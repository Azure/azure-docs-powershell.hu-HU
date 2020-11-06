---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491544"
---
# <span data-ttu-id="2abd8-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="2abd8-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="2abd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2abd8-102">SYNOPSIS</span></span>
<span data-ttu-id="2abd8-103">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="2abd8-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="2abd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2abd8-104">SYNTAX</span></span>

### <span data-ttu-id="2abd8-105">Apply (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2abd8-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abd8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2abd8-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2abd8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2abd8-107">DESCRIPTION</span></span>
<span data-ttu-id="2abd8-108">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="2abd8-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="2abd8-109">A felkérést követően Get-AzsUpdateRun a frissítés folyamatának módosítására is használhatók.</span><span class="sxs-lookup"><span data-stu-id="2abd8-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="2abd8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2abd8-110">EXAMPLES</span></span>

### <span data-ttu-id="2abd8-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2abd8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="2abd8-112">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="2abd8-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="2abd8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2abd8-113">PARAMETERS</span></span>

### <span data-ttu-id="2abd8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2abd8-114">-AsJob</span></span>
<span data-ttu-id="2abd8-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="2abd8-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2abd8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2abd8-116">-Force</span></span>
<span data-ttu-id="2abd8-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2abd8-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2abd8-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="2abd8-118">-Location</span></span>
<span data-ttu-id="2abd8-119">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="2abd8-119">The name of the update location.</span></span>

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

### <span data-ttu-id="2abd8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2abd8-120">-Name</span></span>
<span data-ttu-id="2abd8-121">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="2abd8-121">Name of the update.</span></span>

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

### <span data-ttu-id="2abd8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2abd8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2abd8-123">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="2abd8-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2abd8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2abd8-124">-ResourceId</span></span>
<span data-ttu-id="2abd8-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2abd8-125">The resource id.</span></span>

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

### <span data-ttu-id="2abd8-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2abd8-126">-Confirm</span></span>
<span data-ttu-id="2abd8-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2abd8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2abd8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2abd8-128">-WhatIf</span></span>
<span data-ttu-id="2abd8-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2abd8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2abd8-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2abd8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2abd8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abd8-131">CommonParameters</span></span>
<span data-ttu-id="2abd8-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2abd8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abd8-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2abd8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abd8-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2abd8-134">INPUTS</span></span>

## <span data-ttu-id="2abd8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2abd8-135">OUTPUTS</span></span>

### <span data-ttu-id="2abd8-136">Microsoft. AzureStack. Management. Update. admin. modellek. Update</span><span class="sxs-lookup"><span data-stu-id="2abd8-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="2abd8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2abd8-137">NOTES</span></span>

## <span data-ttu-id="2abd8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2abd8-138">RELATED LINKS</span></span>

