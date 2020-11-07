---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840177"
---
# <span data-ttu-id="77660-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="77660-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="77660-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77660-102">SYNOPSIS</span></span>
<span data-ttu-id="77660-103">A kért infrastruktúra-szerepkör újraindítása.</span><span class="sxs-lookup"><span data-stu-id="77660-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="77660-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77660-104">SYNTAX</span></span>

### <span data-ttu-id="77660-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77660-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77660-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77660-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77660-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="77660-107">DESCRIPTION</span></span>
<span data-ttu-id="77660-108">A kért infrastruktúra-szerepkör újraindítása.</span><span class="sxs-lookup"><span data-stu-id="77660-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="77660-109">Példák</span><span class="sxs-lookup"><span data-stu-id="77660-109">EXAMPLES</span></span>

### <span data-ttu-id="77660-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="77660-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="77660-111">Indítsa újra az infrastrukturális szerepkört, amely összeomlott.</span><span class="sxs-lookup"><span data-stu-id="77660-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="77660-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77660-112">PARAMETERS</span></span>

### <span data-ttu-id="77660-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77660-113">-Name</span></span>
<span data-ttu-id="77660-114">Infrastruktúra-szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="77660-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="77660-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="77660-115">-Location</span></span>
<span data-ttu-id="77660-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="77660-116">Location of the resource.</span></span>

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

### <span data-ttu-id="77660-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77660-117">-ResourceGroupName</span></span>
<span data-ttu-id="77660-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="77660-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="77660-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77660-119">-ResourceId</span></span>
<span data-ttu-id="77660-120">Infrastruktúra-szerepkör erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="77660-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="77660-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77660-121">-AsJob</span></span>
<span data-ttu-id="77660-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="77660-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="77660-123">-Force</span><span class="sxs-lookup"><span data-stu-id="77660-123">-Force</span></span>
<span data-ttu-id="77660-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77660-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="77660-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77660-125">-WhatIf</span></span>
<span data-ttu-id="77660-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77660-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77660-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77660-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77660-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77660-128">-Confirm</span></span>
<span data-ttu-id="77660-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77660-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77660-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77660-130">CommonParameters</span></span>
<span data-ttu-id="77660-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77660-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77660-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77660-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77660-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77660-133">INPUTS</span></span>

## <span data-ttu-id="77660-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77660-134">OUTPUTS</span></span>

## <span data-ttu-id="77660-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77660-135">NOTES</span></span>

## <span data-ttu-id="77660-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77660-136">RELATED LINKS</span></span>
