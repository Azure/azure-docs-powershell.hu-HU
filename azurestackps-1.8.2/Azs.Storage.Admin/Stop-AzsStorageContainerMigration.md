---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016603"
---
# <span data-ttu-id="9204f-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="9204f-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="9204f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9204f-102">SYNOPSIS</span></span>
<span data-ttu-id="9204f-103">Tároló áttelepítési feladatának visszavonása</span><span class="sxs-lookup"><span data-stu-id="9204f-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="9204f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9204f-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9204f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9204f-105">DESCRIPTION</span></span>
<span data-ttu-id="9204f-106">Tároló áttelepítési feladatának visszavonása</span><span class="sxs-lookup"><span data-stu-id="9204f-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="9204f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9204f-107">EXAMPLES</span></span>

### <span data-ttu-id="9204f-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="9204f-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="9204f-109">Tároló áttelepítésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="9204f-109">Cancel container migration.</span></span>

## <span data-ttu-id="9204f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9204f-110">PARAMETERS</span></span>

### <span data-ttu-id="9204f-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="9204f-111">-JobId</span></span>
<span data-ttu-id="9204f-112">Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="9204f-112">Operation Id.</span></span>

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

### <span data-ttu-id="9204f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9204f-113">-ResourceGroupName</span></span>
<span data-ttu-id="9204f-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9204f-114">Resource group name.</span></span>

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

### <span data-ttu-id="9204f-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9204f-115">-FarmName</span></span>
<span data-ttu-id="9204f-116">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="9204f-116">Farm Id.</span></span>

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

### <span data-ttu-id="9204f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9204f-117">-AsJob</span></span>
<span data-ttu-id="9204f-118">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="9204f-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9204f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9204f-119">-Force</span></span>
<span data-ttu-id="9204f-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9204f-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9204f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9204f-121">-WhatIf</span></span>
<span data-ttu-id="9204f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9204f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9204f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9204f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9204f-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9204f-124">-Confirm</span></span>
<span data-ttu-id="9204f-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9204f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9204f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9204f-126">CommonParameters</span></span>
<span data-ttu-id="9204f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9204f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9204f-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9204f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9204f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9204f-129">INPUTS</span></span>

## <span data-ttu-id="9204f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9204f-130">OUTPUTS</span></span>

## <span data-ttu-id="9204f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9204f-131">NOTES</span></span>

## <span data-ttu-id="9204f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9204f-132">RELATED LINKS</span></span>
