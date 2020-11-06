---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5a52ebfe2d59a200add1c8f763f7a3cafa59c18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491400"
---
# <span data-ttu-id="d22f8-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="d22f8-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="d22f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d22f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f8-103">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="d22f8-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="d22f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d22f8-104">SYNTAX</span></span>

### <span data-ttu-id="d22f8-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d22f8-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d22f8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d22f8-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d22f8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d22f8-107">DESCRIPTION</span></span>
<span data-ttu-id="d22f8-108">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="d22f8-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="d22f8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d22f8-109">EXAMPLES</span></span>

### <span data-ttu-id="d22f8-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d22f8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="d22f8-111">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="d22f8-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="d22f8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d22f8-112">PARAMETERS</span></span>

### <span data-ttu-id="d22f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d22f8-113">-AsJob</span></span>
<span data-ttu-id="d22f8-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="d22f8-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d22f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d22f8-115">-Force</span></span>
<span data-ttu-id="d22f8-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d22f8-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d22f8-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="d22f8-117">-Location</span></span>
<span data-ttu-id="d22f8-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d22f8-118">Location of the resource.</span></span>

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

### <span data-ttu-id="d22f8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d22f8-119">-Name</span></span>
<span data-ttu-id="d22f8-120">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="d22f8-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="d22f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="d22f8-122">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="d22f8-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d22f8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d22f8-123">-ResourceId</span></span>
<span data-ttu-id="d22f8-124">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d22f8-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="d22f8-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d22f8-125">-Confirm</span></span>
<span data-ttu-id="d22f8-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d22f8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22f8-127">-WhatIf</span></span>
<span data-ttu-id="d22f8-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d22f8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22f8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d22f8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f8-130">CommonParameters</span></span>
<span data-ttu-id="d22f8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d22f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f8-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22f8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22f8-133">INPUTS</span></span>

## <span data-ttu-id="d22f8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22f8-134">OUTPUTS</span></span>

## <span data-ttu-id="d22f8-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d22f8-135">NOTES</span></span>

## <span data-ttu-id="d22f8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d22f8-136">RELATED LINKS</span></span>

