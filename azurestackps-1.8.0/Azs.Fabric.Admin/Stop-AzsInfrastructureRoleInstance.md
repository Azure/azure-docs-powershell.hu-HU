---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840172"
---
# <span data-ttu-id="5ab81-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="5ab81-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="5ab81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ab81-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab81-103">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="5ab81-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="5ab81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ab81-104">SYNTAX</span></span>

### <span data-ttu-id="5ab81-105">Erő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ab81-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab81-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ab81-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab81-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ab81-107">DESCRIPTION</span></span>
<span data-ttu-id="5ab81-108">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="5ab81-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="5ab81-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5ab81-109">EXAMPLES</span></span>

### <span data-ttu-id="5ab81-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="5ab81-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="5ab81-111">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="5ab81-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="5ab81-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ab81-112">PARAMETERS</span></span>

### <span data-ttu-id="5ab81-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ab81-113">-Name</span></span>
<span data-ttu-id="5ab81-114">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5ab81-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab81-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="5ab81-115">-Location</span></span>
<span data-ttu-id="5ab81-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5ab81-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab81-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab81-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ab81-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="5ab81-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab81-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ab81-119">-ResourceId</span></span>
<span data-ttu-id="5ab81-120">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5ab81-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="5ab81-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ab81-121">-AsJob</span></span>
<span data-ttu-id="5ab81-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="5ab81-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5ab81-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5ab81-123">-Force</span></span>
<span data-ttu-id="5ab81-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ab81-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5ab81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab81-125">-WhatIf</span></span>
<span data-ttu-id="5ab81-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ab81-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab81-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ab81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab81-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ab81-128">-Confirm</span></span>
<span data-ttu-id="5ab81-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ab81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab81-130">CommonParameters</span></span>
<span data-ttu-id="5ab81-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ab81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab81-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab81-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab81-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab81-133">INPUTS</span></span>

## <span data-ttu-id="5ab81-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab81-134">OUTPUTS</span></span>

## <span data-ttu-id="5ab81-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ab81-135">NOTES</span></span>

## <span data-ttu-id="5ab81-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ab81-136">RELATED LINKS</span></span>
