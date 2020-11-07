---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840258"
---
# <span data-ttu-id="a2280-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="a2280-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="a2280-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2280-102">SYNOPSIS</span></span>
<span data-ttu-id="a2280-103">A törölt tárterület-objektumokra vonatkozóan indítsa el a Garbage-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="a2280-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="a2280-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2280-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2280-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2280-105">DESCRIPTION</span></span>
<span data-ttu-id="a2280-106">A törölt tárterület-objektumokra vonatkozóan indítsa el a Garbage-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="a2280-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="a2280-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2280-107">EXAMPLES</span></span>

### <span data-ttu-id="a2280-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2280-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="a2280-109">Indítsa el a Garbage gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="a2280-109">Start garbage collection.</span></span>

## <span data-ttu-id="a2280-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2280-110">PARAMETERS</span></span>

### <span data-ttu-id="a2280-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2280-111">-AsJob</span></span>
<span data-ttu-id="a2280-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="a2280-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a2280-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a2280-113">-FarmName</span></span>
<span data-ttu-id="a2280-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="a2280-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2280-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a2280-115">-Force</span></span>
<span data-ttu-id="a2280-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2280-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2280-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2280-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2280-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a2280-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2280-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2280-119">-Confirm</span></span>
<span data-ttu-id="a2280-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2280-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2280-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2280-121">-WhatIf</span></span>
<span data-ttu-id="a2280-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2280-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2280-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2280-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2280-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2280-124">CommonParameters</span></span>
<span data-ttu-id="a2280-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2280-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2280-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2280-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2280-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2280-127">INPUTS</span></span>

## <span data-ttu-id="a2280-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2280-128">OUTPUTS</span></span>

## <span data-ttu-id="a2280-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2280-129">NOTES</span></span>

## <span data-ttu-id="a2280-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2280-130">RELATED LINKS</span></span>

