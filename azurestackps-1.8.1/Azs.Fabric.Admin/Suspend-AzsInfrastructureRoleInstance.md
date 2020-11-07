---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840885"
---
# <span data-ttu-id="63128-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="63128-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="63128-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63128-102">SYNOPSIS</span></span>
<span data-ttu-id="63128-103">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="63128-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="63128-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63128-104">SYNTAX</span></span>

### <span data-ttu-id="63128-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63128-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63128-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="63128-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63128-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="63128-107">DESCRIPTION</span></span>
<span data-ttu-id="63128-108">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="63128-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="63128-109">Példák</span><span class="sxs-lookup"><span data-stu-id="63128-109">EXAMPLES</span></span>

### <span data-ttu-id="63128-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="63128-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="63128-111">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="63128-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="63128-112">Hiba esetén a program kidobta a kivételt.</span><span class="sxs-lookup"><span data-stu-id="63128-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="63128-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63128-113">PARAMETERS</span></span>

### <span data-ttu-id="63128-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63128-114">-Name</span></span>
<span data-ttu-id="63128-115">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="63128-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63128-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="63128-116">-Location</span></span>
<span data-ttu-id="63128-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="63128-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63128-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63128-118">-ResourceGroupName</span></span>
<span data-ttu-id="63128-119">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="63128-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63128-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63128-120">-ResourceId</span></span>
<span data-ttu-id="63128-121">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="63128-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="63128-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63128-122">-AsJob</span></span>
<span data-ttu-id="63128-123">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="63128-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="63128-124">-Force</span><span class="sxs-lookup"><span data-stu-id="63128-124">-Force</span></span>
<span data-ttu-id="63128-125">Nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="63128-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="63128-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63128-126">-WhatIf</span></span>
<span data-ttu-id="63128-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63128-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63128-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63128-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63128-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63128-129">-Confirm</span></span>
<span data-ttu-id="63128-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63128-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63128-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63128-131">CommonParameters</span></span>
<span data-ttu-id="63128-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63128-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63128-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63128-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63128-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63128-134">INPUTS</span></span>

## <span data-ttu-id="63128-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63128-135">OUTPUTS</span></span>

## <span data-ttu-id="63128-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63128-136">NOTES</span></span>

## <span data-ttu-id="63128-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63128-137">RELATED LINKS</span></span>
