---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840292"
---
# <span data-ttu-id="dd8b4-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dd8b4-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="dd8b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8b4-103">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="dd8b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd8b4-104">SYNTAX</span></span>

### <span data-ttu-id="dd8b4-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd8b4-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd8b4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd8b4-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd8b4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd8b4-107">DESCRIPTION</span></span>
<span data-ttu-id="dd8b4-108">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="dd8b4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd8b4-109">EXAMPLES</span></span>

### <span data-ttu-id="dd8b4-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="dd8b4-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="dd8b4-111">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="dd8b4-112">Hiba esetén a program kidobta a kivételt.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="dd8b4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd8b4-113">PARAMETERS</span></span>

### <span data-ttu-id="dd8b4-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd8b4-114">-Name</span></span>
<span data-ttu-id="dd8b4-115">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-115">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="dd8b4-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="dd8b4-116">-Location</span></span>
<span data-ttu-id="dd8b4-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-117">Location of the resource.</span></span>

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

### <span data-ttu-id="dd8b4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8b4-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd8b4-119">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="dd8b4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd8b4-120">-ResourceId</span></span>
<span data-ttu-id="dd8b4-121">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="dd8b4-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd8b4-122">-AsJob</span></span>
<span data-ttu-id="dd8b4-123">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="dd8b4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dd8b4-124">-Force</span></span>
<span data-ttu-id="dd8b4-125">Nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="dd8b4-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="dd8b4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8b4-126">-WhatIf</span></span>
<span data-ttu-id="dd8b4-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8b4-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8b4-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd8b4-129">-Confirm</span></span>
<span data-ttu-id="dd8b4-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd8b4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8b4-131">CommonParameters</span></span>
<span data-ttu-id="dd8b4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd8b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8b4-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8b4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8b4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd8b4-134">INPUTS</span></span>

## <span data-ttu-id="dd8b4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd8b4-135">OUTPUTS</span></span>

## <span data-ttu-id="dd8b4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd8b4-136">NOTES</span></span>

## <span data-ttu-id="dd8b4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd8b4-137">RELATED LINKS</span></span>
