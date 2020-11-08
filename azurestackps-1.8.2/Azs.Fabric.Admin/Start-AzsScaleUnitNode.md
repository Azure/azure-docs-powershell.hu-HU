---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016839"
---
# <span data-ttu-id="a5c10-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="a5c10-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="a5c10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5c10-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c10-103">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="a5c10-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="a5c10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5c10-104">SYNTAX</span></span>

### <span data-ttu-id="a5c10-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5c10-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c10-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c10-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c10-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5c10-107">DESCRIPTION</span></span>
<span data-ttu-id="a5c10-108">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="a5c10-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="a5c10-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a5c10-109">EXAMPLES</span></span>

### <span data-ttu-id="a5c10-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="a5c10-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="a5c10-111">ProvisioningState: sikerült</span><span class="sxs-lookup"><span data-stu-id="a5c10-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="a5c10-112">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="a5c10-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="a5c10-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5c10-113">PARAMETERS</span></span>

### <span data-ttu-id="a5c10-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5c10-114">-Name</span></span>
<span data-ttu-id="a5c10-115">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="a5c10-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="a5c10-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5c10-116">-Location</span></span>
<span data-ttu-id="a5c10-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a5c10-117">Location of the resource.</span></span>

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

### <span data-ttu-id="a5c10-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c10-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5c10-119">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="a5c10-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a5c10-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c10-120">-ResourceId</span></span>
<span data-ttu-id="a5c10-121">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a5c10-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="a5c10-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c10-122">-AsJob</span></span>
<span data-ttu-id="a5c10-123">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="a5c10-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a5c10-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c10-124">-Force</span></span>
<span data-ttu-id="a5c10-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5c10-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a5c10-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c10-126">-WhatIf</span></span>
<span data-ttu-id="a5c10-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5c10-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c10-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5c10-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c10-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5c10-129">-Confirm</span></span>
<span data-ttu-id="a5c10-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5c10-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c10-131">CommonParameters</span></span>
<span data-ttu-id="a5c10-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5c10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c10-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c10-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c10-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c10-134">INPUTS</span></span>

## <span data-ttu-id="a5c10-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c10-135">OUTPUTS</span></span>

## <span data-ttu-id="a5c10-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5c10-136">NOTES</span></span>

## <span data-ttu-id="a5c10-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5c10-137">RELATED LINKS</span></span>
