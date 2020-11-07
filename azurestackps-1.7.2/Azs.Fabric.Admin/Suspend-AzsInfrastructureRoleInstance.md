---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840034"
---
# <span data-ttu-id="8e96d-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="8e96d-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="8e96d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e96d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e96d-103">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="8e96d-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="8e96d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e96d-104">SYNTAX</span></span>

### <span data-ttu-id="8e96d-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e96d-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e96d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e96d-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e96d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e96d-107">DESCRIPTION</span></span>
<span data-ttu-id="8e96d-108">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="8e96d-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="8e96d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e96d-109">EXAMPLES</span></span>

### <span data-ttu-id="8e96d-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e96d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="8e96d-111">Állítsa le az infrastruktúra szerepkör-példányát.</span><span class="sxs-lookup"><span data-stu-id="8e96d-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="8e96d-112">Hiba esetén a program kidobta a kivételt.</span><span class="sxs-lookup"><span data-stu-id="8e96d-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="8e96d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e96d-113">PARAMETERS</span></span>

### <span data-ttu-id="8e96d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e96d-114">-AsJob</span></span>
<span data-ttu-id="8e96d-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="8e96d-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8e96d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8e96d-116">-Force</span></span>
<span data-ttu-id="8e96d-117">Nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="8e96d-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="8e96d-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="8e96d-118">-Location</span></span>
<span data-ttu-id="8e96d-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8e96d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8e96d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e96d-120">-Name</span></span>
<span data-ttu-id="8e96d-121">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="8e96d-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="8e96d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e96d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e96d-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="8e96d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8e96d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e96d-124">-ResourceId</span></span>
<span data-ttu-id="8e96d-125">Infrastruktúra szerepkör-példány erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e96d-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="8e96d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e96d-126">-Confirm</span></span>
<span data-ttu-id="8e96d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e96d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e96d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e96d-128">-WhatIf</span></span>
<span data-ttu-id="8e96d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e96d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e96d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e96d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e96d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e96d-131">CommonParameters</span></span>
<span data-ttu-id="8e96d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e96d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e96d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e96d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e96d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e96d-134">INPUTS</span></span>

## <span data-ttu-id="8e96d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e96d-135">OUTPUTS</span></span>

## <span data-ttu-id="8e96d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e96d-136">NOTES</span></span>

## <span data-ttu-id="8e96d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e96d-137">RELATED LINKS</span></span>

