---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016880"
---
# <span data-ttu-id="fe2b0-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="fe2b0-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="fe2b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2b0-103">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="fe2b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe2b0-104">SYNTAX</span></span>

### <span data-ttu-id="fe2b0-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe2b0-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2b0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2b0-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe2b0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe2b0-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2b0-108">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="fe2b0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fe2b0-109">EXAMPLES</span></span>

### <span data-ttu-id="fe2b0-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="fe2b0-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="fe2b0-111">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="fe2b0-112">Hiba esetén a program kidobta a kivételt.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="fe2b0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe2b0-113">PARAMETERS</span></span>

### <span data-ttu-id="fe2b0-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe2b0-114">-Name</span></span>
<span data-ttu-id="fe2b0-115">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-115">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="fe2b0-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="fe2b0-116">-Location</span></span>
<span data-ttu-id="fe2b0-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-117">Location of the resource.</span></span>

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

### <span data-ttu-id="fe2b0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2b0-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe2b0-119">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="fe2b0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2b0-120">-ResourceId</span></span>
<span data-ttu-id="fe2b0-121">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="fe2b0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe2b0-122">-AsJob</span></span>
<span data-ttu-id="fe2b0-123">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fe2b0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fe2b0-124">-Force</span></span>
<span data-ttu-id="fe2b0-125">Nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="fe2b0-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="fe2b0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2b0-126">-WhatIf</span></span>
<span data-ttu-id="fe2b0-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2b0-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2b0-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe2b0-129">-Confirm</span></span>
<span data-ttu-id="fe2b0-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe2b0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2b0-131">CommonParameters</span></span>
<span data-ttu-id="fe2b0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe2b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2b0-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2b0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2b0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe2b0-134">INPUTS</span></span>

## <span data-ttu-id="fe2b0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe2b0-135">OUTPUTS</span></span>

## <span data-ttu-id="fe2b0-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe2b0-136">NOTES</span></span>

## <span data-ttu-id="fe2b0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe2b0-137">RELATED LINKS</span></span>
