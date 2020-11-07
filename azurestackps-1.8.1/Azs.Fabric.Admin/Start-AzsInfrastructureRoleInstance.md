---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840464"
---
# <span data-ttu-id="2453f-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="2453f-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="2453f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2453f-102">SYNOPSIS</span></span>
<span data-ttu-id="2453f-103">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="2453f-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="2453f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2453f-104">SYNTAX</span></span>

### <span data-ttu-id="2453f-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2453f-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2453f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2453f-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2453f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2453f-107">DESCRIPTION</span></span>
<span data-ttu-id="2453f-108">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="2453f-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="2453f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2453f-109">EXAMPLES</span></span>

### <span data-ttu-id="2453f-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="2453f-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="2453f-111">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="2453f-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="2453f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2453f-112">PARAMETERS</span></span>

### <span data-ttu-id="2453f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2453f-113">-Name</span></span>
<span data-ttu-id="2453f-114">Az infrastrukturális szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="2453f-114">Name of the infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2453f-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="2453f-115">-Location</span></span>
<span data-ttu-id="2453f-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="2453f-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2453f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2453f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2453f-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="2453f-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2453f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2453f-119">-ResourceId</span></span>
<span data-ttu-id="2453f-120">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2453f-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="2453f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2453f-121">-AsJob</span></span>
<span data-ttu-id="2453f-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="2453f-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2453f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2453f-123">-Force</span></span>
<span data-ttu-id="2453f-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2453f-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2453f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2453f-125">-WhatIf</span></span>
<span data-ttu-id="2453f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2453f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2453f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2453f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2453f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2453f-128">-Confirm</span></span>
<span data-ttu-id="2453f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2453f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2453f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2453f-130">CommonParameters</span></span>
<span data-ttu-id="2453f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2453f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2453f-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2453f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2453f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2453f-133">INPUTS</span></span>

## <span data-ttu-id="2453f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2453f-134">OUTPUTS</span></span>

## <span data-ttu-id="2453f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2453f-135">NOTES</span></span>

## <span data-ttu-id="2453f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2453f-136">RELATED LINKS</span></span>
