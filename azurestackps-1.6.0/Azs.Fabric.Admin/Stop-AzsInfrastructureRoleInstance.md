---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671760"
---
# <span data-ttu-id="49bd7-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="49bd7-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="49bd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="49bd7-103">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="49bd7-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="49bd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49bd7-104">SYNTAX</span></span>

### <span data-ttu-id="49bd7-105">Erő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49bd7-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49bd7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="49bd7-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49bd7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="49bd7-107">DESCRIPTION</span></span>
<span data-ttu-id="49bd7-108">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="49bd7-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="49bd7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="49bd7-109">EXAMPLES</span></span>

### <span data-ttu-id="49bd7-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49bd7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="49bd7-111">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="49bd7-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="49bd7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49bd7-112">PARAMETERS</span></span>

### <span data-ttu-id="49bd7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49bd7-113">-AsJob</span></span>
<span data-ttu-id="49bd7-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="49bd7-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="49bd7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="49bd7-115">-Force</span></span>
<span data-ttu-id="49bd7-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49bd7-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="49bd7-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="49bd7-117">-Location</span></span>
<span data-ttu-id="49bd7-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="49bd7-118">Location of the resource.</span></span>

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

### <span data-ttu-id="49bd7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49bd7-119">-Name</span></span>
<span data-ttu-id="49bd7-120">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="49bd7-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="49bd7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bd7-121">-ResourceGroupName</span></span>
<span data-ttu-id="49bd7-122">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="49bd7-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="49bd7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49bd7-123">-ResourceId</span></span>
<span data-ttu-id="49bd7-124">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="49bd7-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="49bd7-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49bd7-125">-Confirm</span></span>
<span data-ttu-id="49bd7-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49bd7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bd7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bd7-127">-WhatIf</span></span>
<span data-ttu-id="49bd7-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49bd7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49bd7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49bd7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bd7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bd7-130">CommonParameters</span></span>
<span data-ttu-id="49bd7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49bd7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bd7-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49bd7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bd7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49bd7-133">INPUTS</span></span>

## <span data-ttu-id="49bd7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49bd7-134">OUTPUTS</span></span>

## <span data-ttu-id="49bd7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49bd7-135">NOTES</span></span>

## <span data-ttu-id="49bd7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49bd7-136">RELATED LINKS</span></span>

