---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840905"
---
# <span data-ttu-id="1822a-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1822a-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1822a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1822a-102">SYNOPSIS</span></span>
<span data-ttu-id="1822a-103">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="1822a-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="1822a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1822a-104">SYNTAX</span></span>

### <span data-ttu-id="1822a-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1822a-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1822a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1822a-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1822a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1822a-107">DESCRIPTION</span></span>
<span data-ttu-id="1822a-108">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="1822a-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="1822a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1822a-109">EXAMPLES</span></span>

### <span data-ttu-id="1822a-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="1822a-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="1822a-111">ProvisioningState: sikerült</span><span class="sxs-lookup"><span data-stu-id="1822a-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="1822a-112">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="1822a-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="1822a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1822a-113">PARAMETERS</span></span>

### <span data-ttu-id="1822a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1822a-114">-Name</span></span>
<span data-ttu-id="1822a-115">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="1822a-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1822a-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="1822a-116">-Location</span></span>
<span data-ttu-id="1822a-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1822a-117">Location of the resource.</span></span>

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

### <span data-ttu-id="1822a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1822a-118">-ResourceGroupName</span></span>
<span data-ttu-id="1822a-119">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="1822a-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1822a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1822a-120">-ResourceId</span></span>
<span data-ttu-id="1822a-121">Egységösszeg-csomópont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1822a-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1822a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1822a-122">-AsJob</span></span>
<span data-ttu-id="1822a-123">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="1822a-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1822a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1822a-124">-Force</span></span>
<span data-ttu-id="1822a-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1822a-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1822a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1822a-126">-WhatIf</span></span>
<span data-ttu-id="1822a-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1822a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1822a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1822a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1822a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1822a-129">-Confirm</span></span>
<span data-ttu-id="1822a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1822a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1822a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1822a-131">CommonParameters</span></span>
<span data-ttu-id="1822a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1822a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1822a-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1822a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1822a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1822a-134">INPUTS</span></span>

## <span data-ttu-id="1822a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1822a-135">OUTPUTS</span></span>

## <span data-ttu-id="1822a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1822a-136">NOTES</span></span>

## <span data-ttu-id="1822a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1822a-137">RELATED LINKS</span></span>
