---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490895"
---
# <span data-ttu-id="71582-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="71582-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="71582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71582-102">SYNOPSIS</span></span>
<span data-ttu-id="71582-103">A kért infrastrukturális szerepkör újraindítása.</span><span class="sxs-lookup"><span data-stu-id="71582-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="71582-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71582-104">SYNTAX</span></span>

### <span data-ttu-id="71582-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71582-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71582-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="71582-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71582-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="71582-107">DESCRIPTION</span></span>
<span data-ttu-id="71582-108">A kért infrastrukturális szerepkör újraindítása.</span><span class="sxs-lookup"><span data-stu-id="71582-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="71582-109">Példák</span><span class="sxs-lookup"><span data-stu-id="71582-109">EXAMPLES</span></span>

### <span data-ttu-id="71582-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="71582-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="71582-111">Indítsa újra az infrastrukturális szerepkört, amely összeomlott.</span><span class="sxs-lookup"><span data-stu-id="71582-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="71582-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71582-112">PARAMETERS</span></span>

### <span data-ttu-id="71582-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71582-113">-AsJob</span></span>
<span data-ttu-id="71582-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="71582-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="71582-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71582-115">-Force</span></span>
<span data-ttu-id="71582-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71582-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="71582-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="71582-117">-Location</span></span>
<span data-ttu-id="71582-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="71582-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71582-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71582-119">-Name</span></span>
<span data-ttu-id="71582-120">Infrastruktúra-szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="71582-120">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71582-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71582-121">-ResourceGroupName</span></span>
<span data-ttu-id="71582-122">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="71582-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71582-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71582-123">-ResourceId</span></span>
<span data-ttu-id="71582-124">Infrastruktúra-szerepkör erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="71582-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="71582-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71582-125">-Confirm</span></span>
<span data-ttu-id="71582-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71582-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71582-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71582-127">-WhatIf</span></span>
<span data-ttu-id="71582-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71582-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71582-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71582-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71582-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71582-130">CommonParameters</span></span>
<span data-ttu-id="71582-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71582-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71582-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71582-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71582-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71582-133">INPUTS</span></span>

## <span data-ttu-id="71582-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71582-134">OUTPUTS</span></span>

## <span data-ttu-id="71582-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71582-135">NOTES</span></span>

## <span data-ttu-id="71582-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71582-136">RELATED LINKS</span></span>

