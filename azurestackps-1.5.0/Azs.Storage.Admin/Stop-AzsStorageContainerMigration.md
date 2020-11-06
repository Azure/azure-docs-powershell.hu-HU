---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490700"
---
# <span data-ttu-id="48d6b-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="48d6b-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="48d6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="48d6b-103">Tároló áttelepítési feladatának visszavonása</span><span class="sxs-lookup"><span data-stu-id="48d6b-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="48d6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48d6b-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="48d6b-106">Tároló áttelepítési feladatának visszavonása</span><span class="sxs-lookup"><span data-stu-id="48d6b-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="48d6b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="48d6b-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="48d6b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="48d6b-109">Tároló áttelepítésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="48d6b-109">Cancel container migration.</span></span>

## <span data-ttu-id="48d6b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48d6b-110">PARAMETERS</span></span>

### <span data-ttu-id="48d6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48d6b-111">-AsJob</span></span>
<span data-ttu-id="48d6b-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="48d6b-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="48d6b-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="48d6b-113">-FarmName</span></span>
<span data-ttu-id="48d6b-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="48d6b-114">Farm Id.</span></span>

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

### <span data-ttu-id="48d6b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="48d6b-115">-Force</span></span>
<span data-ttu-id="48d6b-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48d6b-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48d6b-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="48d6b-117">-JobId</span></span>
<span data-ttu-id="48d6b-118">Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="48d6b-118">Operation Id.</span></span>

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

### <span data-ttu-id="48d6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="48d6b-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="48d6b-120">Resource group name.</span></span>

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

### <span data-ttu-id="48d6b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48d6b-121">-Confirm</span></span>
<span data-ttu-id="48d6b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48d6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d6b-123">-WhatIf</span></span>
<span data-ttu-id="48d6b-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48d6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48d6b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48d6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d6b-126">CommonParameters</span></span>
<span data-ttu-id="48d6b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48d6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d6b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d6b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d6b-129">INPUTS</span></span>

## <span data-ttu-id="48d6b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d6b-130">OUTPUTS</span></span>

## <span data-ttu-id="48d6b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48d6b-131">NOTES</span></span>

## <span data-ttu-id="48d6b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48d6b-132">RELATED LINKS</span></span>

