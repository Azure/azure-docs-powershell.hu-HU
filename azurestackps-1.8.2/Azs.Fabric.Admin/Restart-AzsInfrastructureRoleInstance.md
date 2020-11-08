---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016680"
---
# <span data-ttu-id="60cf7-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="60cf7-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="60cf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="60cf7-103">Indítsa újra az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="60cf7-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="60cf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60cf7-104">SYNTAX</span></span>

### <span data-ttu-id="60cf7-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60cf7-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60cf7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="60cf7-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60cf7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60cf7-107">DESCRIPTION</span></span>
<span data-ttu-id="60cf7-108">Indítsa újra az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="60cf7-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="60cf7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="60cf7-109">EXAMPLES</span></span>

### <span data-ttu-id="60cf7-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="60cf7-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="60cf7-111">Indítsa újra az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="60cf7-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="60cf7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60cf7-112">PARAMETERS</span></span>

### <span data-ttu-id="60cf7-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60cf7-113">-Name</span></span>
<span data-ttu-id="60cf7-114">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="60cf7-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="60cf7-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="60cf7-115">-Location</span></span>
<span data-ttu-id="60cf7-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="60cf7-116">Location of the resource.</span></span>

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

### <span data-ttu-id="60cf7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cf7-117">-ResourceGroupName</span></span>
<span data-ttu-id="60cf7-118">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="60cf7-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="60cf7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60cf7-119">-ResourceId</span></span>
<span data-ttu-id="60cf7-120">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="60cf7-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="60cf7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60cf7-121">-AsJob</span></span>
<span data-ttu-id="60cf7-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="60cf7-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="60cf7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="60cf7-123">-Force</span></span>
<span data-ttu-id="60cf7-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60cf7-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="60cf7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60cf7-125">-WhatIf</span></span>
<span data-ttu-id="60cf7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60cf7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60cf7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60cf7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60cf7-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60cf7-128">-Confirm</span></span>
<span data-ttu-id="60cf7-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60cf7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60cf7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cf7-130">CommonParameters</span></span>
<span data-ttu-id="60cf7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60cf7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cf7-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60cf7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cf7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60cf7-133">INPUTS</span></span>

## <span data-ttu-id="60cf7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60cf7-134">OUTPUTS</span></span>

## <span data-ttu-id="60cf7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60cf7-135">NOTES</span></span>

## <span data-ttu-id="60cf7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60cf7-136">RELATED LINKS</span></span>
