---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491364"
---
# <span data-ttu-id="14cc6-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="14cc6-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="14cc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="14cc6-103">Az adott riasztás kijavítása.</span><span class="sxs-lookup"><span data-stu-id="14cc6-103">Repairs the given alert.</span></span>

## <span data-ttu-id="14cc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14cc6-104">SYNTAX</span></span>

### <span data-ttu-id="14cc6-105">Javítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14cc6-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14cc6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="14cc6-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14cc6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="14cc6-107">DESCRIPTION</span></span>
<span data-ttu-id="14cc6-108">Az adott riasztás kijavítása.</span><span class="sxs-lookup"><span data-stu-id="14cc6-108">Repairs the given alert.</span></span>

## <span data-ttu-id="14cc6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="14cc6-109">EXAMPLES</span></span>

### <span data-ttu-id="14cc6-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14cc6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="14cc6-111">Riasztás kijavítása név szerint</span><span class="sxs-lookup"><span data-stu-id="14cc6-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="14cc6-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="14cc6-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="14cc6-113">A csöveken keresztüli riasztás kijavítása.</span><span class="sxs-lookup"><span data-stu-id="14cc6-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="14cc6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14cc6-114">PARAMETERS</span></span>

### <span data-ttu-id="14cc6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="14cc6-115">-Force</span></span>
<span data-ttu-id="14cc6-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14cc6-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="14cc6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14cc6-117">-InputObject</span></span>
<span data-ttu-id="14cc6-118">A Get-AzsAlert kapott riasztás.</span><span class="sxs-lookup"><span data-stu-id="14cc6-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14cc6-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="14cc6-119">-Location</span></span>
<span data-ttu-id="14cc6-120">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="14cc6-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14cc6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14cc6-121">-Name</span></span>
<span data-ttu-id="14cc6-122">Az értesítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14cc6-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14cc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14cc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="14cc6-124">Erőforráscsoport neve, amely az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="14cc6-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14cc6-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14cc6-125">-Confirm</span></span>
<span data-ttu-id="14cc6-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14cc6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14cc6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14cc6-127">-WhatIf</span></span>
<span data-ttu-id="14cc6-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14cc6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14cc6-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14cc6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14cc6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cc6-130">CommonParameters</span></span>
<span data-ttu-id="14cc6-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14cc6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14cc6-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14cc6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cc6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14cc6-133">INPUTS</span></span>

## <span data-ttu-id="14cc6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14cc6-134">OUTPUTS</span></span>

## <span data-ttu-id="14cc6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14cc6-135">NOTES</span></span>

## <span data-ttu-id="14cc6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14cc6-136">RELATED LINKS</span></span>

