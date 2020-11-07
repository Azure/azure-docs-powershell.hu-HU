---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840024"
---
# <span data-ttu-id="bad6b-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="bad6b-101">Close-AzsAlert</span></span>

## <span data-ttu-id="bad6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="bad6b-103">Bezárja az adott riasztást.</span><span class="sxs-lookup"><span data-stu-id="bad6b-103">Closes the given alert.</span></span>

## <span data-ttu-id="bad6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bad6b-104">SYNTAX</span></span>

### <span data-ttu-id="bad6b-105">Bezárás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bad6b-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bad6b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bad6b-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bad6b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bad6b-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bad6b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bad6b-108">DESCRIPTION</span></span>
<span data-ttu-id="bad6b-109">Bezárja az adott riasztást.</span><span class="sxs-lookup"><span data-stu-id="bad6b-109">Closes the given alert.</span></span>

## <span data-ttu-id="bad6b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bad6b-110">EXAMPLES</span></span>

### <span data-ttu-id="bad6b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bad6b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="bad6b-112">Riasztás megszüntetése név szerint</span><span class="sxs-lookup"><span data-stu-id="bad6b-112">Close an alert by Name.</span></span>

### <span data-ttu-id="bad6b-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bad6b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="bad6b-114">Riasztást az adatcsöveken keresztül zárhatja be.</span><span class="sxs-lookup"><span data-stu-id="bad6b-114">Close an alert through piping.</span></span>

## <span data-ttu-id="bad6b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bad6b-115">PARAMETERS</span></span>

### <span data-ttu-id="bad6b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bad6b-116">-Force</span></span>
<span data-ttu-id="bad6b-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bad6b-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bad6b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bad6b-118">-InputObject</span></span>
<span data-ttu-id="bad6b-119">A Get-AzsAlert kapott riasztás.</span><span class="sxs-lookup"><span data-stu-id="bad6b-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="bad6b-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="bad6b-120">-Location</span></span>
<span data-ttu-id="bad6b-121">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="bad6b-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad6b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bad6b-122">-Name</span></span>
<span data-ttu-id="bad6b-123">Az értesítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bad6b-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bad6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="bad6b-125">Erőforráscsoport neve, amely az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="bad6b-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad6b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bad6b-126">-ResourceId</span></span>
<span data-ttu-id="bad6b-127">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bad6b-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad6b-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bad6b-128">-Confirm</span></span>
<span data-ttu-id="bad6b-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bad6b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bad6b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bad6b-130">-WhatIf</span></span>
<span data-ttu-id="bad6b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bad6b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bad6b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bad6b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bad6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad6b-133">CommonParameters</span></span>
<span data-ttu-id="bad6b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bad6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad6b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad6b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad6b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bad6b-136">INPUTS</span></span>

## <span data-ttu-id="bad6b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bad6b-137">OUTPUTS</span></span>

### <span data-ttu-id="bad6b-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. riasztás</span><span class="sxs-lookup"><span data-stu-id="bad6b-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="bad6b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bad6b-139">NOTES</span></span>

## <span data-ttu-id="bad6b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bad6b-140">RELATED LINKS</span></span>

