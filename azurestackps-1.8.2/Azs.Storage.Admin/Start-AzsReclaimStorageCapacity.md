---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016952"
---
# <span data-ttu-id="03c34-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="03c34-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="03c34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03c34-102">SYNOPSIS</span></span>
<span data-ttu-id="03c34-103">A törölt tárterület-objektumokra vonatkozóan indítsa el a Garbage-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="03c34-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="03c34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03c34-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03c34-105">DESCRIPTION</span></span>
<span data-ttu-id="03c34-106">A törölt tárterület-objektumokra vonatkozóan indítsa el a Garbage-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="03c34-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="03c34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03c34-107">EXAMPLES</span></span>

### <span data-ttu-id="03c34-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="03c34-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="03c34-109">Indítsa el a Garbage gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="03c34-109">Start garbage collection.</span></span>

## <span data-ttu-id="03c34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03c34-110">PARAMETERS</span></span>

### <span data-ttu-id="03c34-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c34-111">-ResourceGroupName</span></span>
<span data-ttu-id="03c34-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="03c34-112">Resource group name.</span></span>

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

### <span data-ttu-id="03c34-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="03c34-113">-FarmName</span></span>
<span data-ttu-id="03c34-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="03c34-114">Farm Id.</span></span>

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

### <span data-ttu-id="03c34-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c34-115">-AsJob</span></span>
<span data-ttu-id="03c34-116">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="03c34-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="03c34-117">-Force</span><span class="sxs-lookup"><span data-stu-id="03c34-117">-Force</span></span>
<span data-ttu-id="03c34-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03c34-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="03c34-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c34-119">-WhatIf</span></span>
<span data-ttu-id="03c34-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03c34-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c34-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03c34-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c34-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03c34-122">-Confirm</span></span>
<span data-ttu-id="03c34-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03c34-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c34-124">CommonParameters</span></span>
<span data-ttu-id="03c34-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03c34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c34-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c34-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c34-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03c34-127">INPUTS</span></span>

## <span data-ttu-id="03c34-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03c34-128">OUTPUTS</span></span>

## <span data-ttu-id="03c34-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03c34-129">NOTES</span></span>

## <span data-ttu-id="03c34-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03c34-130">RELATED LINKS</span></span>
