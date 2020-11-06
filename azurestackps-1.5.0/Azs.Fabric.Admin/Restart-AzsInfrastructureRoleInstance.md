---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6e7801a2188fe80577bc6cef9315069b0207f91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490892"
---
# <span data-ttu-id="699ca-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="699ca-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="699ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="699ca-102">SYNOPSIS</span></span>
<span data-ttu-id="699ca-103">Indítsa újra az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="699ca-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="699ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="699ca-104">SYNTAX</span></span>

### <span data-ttu-id="699ca-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="699ca-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="699ca-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="699ca-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="699ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="699ca-107">DESCRIPTION</span></span>
<span data-ttu-id="699ca-108">Indítsa újra az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="699ca-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="699ca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="699ca-109">EXAMPLES</span></span>

### <span data-ttu-id="699ca-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="699ca-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="699ca-111">Indítsa újra az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="699ca-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="699ca-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="699ca-112">PARAMETERS</span></span>

### <span data-ttu-id="699ca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="699ca-113">-AsJob</span></span>
<span data-ttu-id="699ca-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="699ca-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="699ca-115">-Force</span><span class="sxs-lookup"><span data-stu-id="699ca-115">-Force</span></span>
<span data-ttu-id="699ca-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="699ca-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="699ca-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="699ca-117">-Location</span></span>
<span data-ttu-id="699ca-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="699ca-118">Location of the resource.</span></span>

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

### <span data-ttu-id="699ca-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="699ca-119">-Name</span></span>
<span data-ttu-id="699ca-120">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="699ca-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="699ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="699ca-122">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="699ca-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="699ca-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="699ca-123">-ResourceId</span></span>
<span data-ttu-id="699ca-124">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="699ca-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="699ca-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="699ca-125">-Confirm</span></span>
<span data-ttu-id="699ca-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="699ca-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="699ca-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699ca-127">-WhatIf</span></span>
<span data-ttu-id="699ca-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="699ca-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="699ca-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="699ca-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="699ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699ca-130">CommonParameters</span></span>
<span data-ttu-id="699ca-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="699ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699ca-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699ca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699ca-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="699ca-133">INPUTS</span></span>

## <span data-ttu-id="699ca-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="699ca-134">OUTPUTS</span></span>

## <span data-ttu-id="699ca-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="699ca-135">NOTES</span></span>

## <span data-ttu-id="699ca-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="699ca-136">RELATED LINKS</span></span>

