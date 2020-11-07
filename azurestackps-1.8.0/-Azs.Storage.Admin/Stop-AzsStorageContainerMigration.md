---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840400"
---
# <span data-ttu-id="45626-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="45626-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="45626-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45626-102">SYNOPSIS</span></span>
<span data-ttu-id="45626-103">Tároló áttelepítési feladatának visszavonása</span><span class="sxs-lookup"><span data-stu-id="45626-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="45626-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45626-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45626-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45626-105">DESCRIPTION</span></span>
<span data-ttu-id="45626-106">Tároló áttelepítési feladatának visszavonása</span><span class="sxs-lookup"><span data-stu-id="45626-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="45626-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45626-107">EXAMPLES</span></span>

### <span data-ttu-id="45626-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45626-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="45626-109">Tároló áttelepítésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="45626-109">Cancel container migration.</span></span>

## <span data-ttu-id="45626-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45626-110">PARAMETERS</span></span>

### <span data-ttu-id="45626-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45626-111">-AsJob</span></span>
<span data-ttu-id="45626-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="45626-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="45626-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="45626-113">-FarmName</span></span>
<span data-ttu-id="45626-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="45626-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45626-115">-Force</span><span class="sxs-lookup"><span data-stu-id="45626-115">-Force</span></span>
<span data-ttu-id="45626-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45626-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="45626-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="45626-117">-JobId</span></span>
<span data-ttu-id="45626-118">Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="45626-118">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45626-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45626-119">-ResourceGroupName</span></span>
<span data-ttu-id="45626-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="45626-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45626-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45626-121">-Confirm</span></span>
<span data-ttu-id="45626-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45626-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45626-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45626-123">-WhatIf</span></span>
<span data-ttu-id="45626-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45626-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45626-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45626-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45626-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45626-126">CommonParameters</span></span>
<span data-ttu-id="45626-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45626-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45626-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45626-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45626-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45626-129">INPUTS</span></span>

## <span data-ttu-id="45626-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45626-130">OUTPUTS</span></span>

## <span data-ttu-id="45626-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45626-131">NOTES</span></span>

## <span data-ttu-id="45626-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45626-132">RELATED LINKS</span></span>

