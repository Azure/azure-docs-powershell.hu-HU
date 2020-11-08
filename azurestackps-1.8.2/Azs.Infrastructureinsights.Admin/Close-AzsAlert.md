---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016922"
---
# <span data-ttu-id="98822-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="98822-101">Close-AzsAlert</span></span>

## <span data-ttu-id="98822-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98822-102">SYNOPSIS</span></span>
<span data-ttu-id="98822-103">Bezárja az adott riasztást.</span><span class="sxs-lookup"><span data-stu-id="98822-103">Closes the given alert.</span></span>

## <span data-ttu-id="98822-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98822-104">SYNTAX</span></span>

### <span data-ttu-id="98822-105">Bezárás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98822-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98822-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="98822-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98822-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="98822-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98822-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="98822-108">DESCRIPTION</span></span>
<span data-ttu-id="98822-109">Bezárja az adott riasztást.</span><span class="sxs-lookup"><span data-stu-id="98822-109">Closes the given alert.</span></span>

## <span data-ttu-id="98822-110">Példák</span><span class="sxs-lookup"><span data-stu-id="98822-110">EXAMPLES</span></span>

### <span data-ttu-id="98822-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="98822-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="98822-112">Riasztás megszüntetése név szerint</span><span class="sxs-lookup"><span data-stu-id="98822-112">Close an alert by Name.</span></span>

### <span data-ttu-id="98822-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="98822-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="98822-114">Riasztást az adatcsöveken keresztül zárhatja be.</span><span class="sxs-lookup"><span data-stu-id="98822-114">Close an alert through piping.</span></span>

## <span data-ttu-id="98822-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98822-115">PARAMETERS</span></span>

### <span data-ttu-id="98822-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98822-116">-Name</span></span>
<span data-ttu-id="98822-117">Az értesítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="98822-117">The alert identifier.</span></span>

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

### <span data-ttu-id="98822-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="98822-118">-Location</span></span>
<span data-ttu-id="98822-119">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="98822-119">Name of the location.</span></span>

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

### <span data-ttu-id="98822-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98822-120">-ResourceGroupName</span></span>
<span data-ttu-id="98822-121">A riasztás erőforrás-csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="98822-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="98822-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98822-122">-InputObject</span></span>
<span data-ttu-id="98822-123">A Get-AzsAlert kapott riasztás.</span><span class="sxs-lookup"><span data-stu-id="98822-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="98822-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98822-124">-ResourceId</span></span>
<span data-ttu-id="98822-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="98822-125">The resource id.</span></span>

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

### <span data-ttu-id="98822-126">-Force</span><span class="sxs-lookup"><span data-stu-id="98822-126">-Force</span></span>
<span data-ttu-id="98822-127">Kapcsoló paraméter a megerősítést kérő üzenet mellőzéséhez.</span><span class="sxs-lookup"><span data-stu-id="98822-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="98822-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98822-128">-WhatIf</span></span>
<span data-ttu-id="98822-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98822-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98822-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98822-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98822-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98822-131">-Confirm</span></span>
<span data-ttu-id="98822-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98822-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98822-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98822-133">CommonParameters</span></span>
<span data-ttu-id="98822-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98822-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98822-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98822-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98822-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98822-136">INPUTS</span></span>

## <span data-ttu-id="98822-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98822-137">OUTPUTS</span></span>

### <span data-ttu-id="98822-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. riasztás</span><span class="sxs-lookup"><span data-stu-id="98822-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="98822-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98822-139">NOTES</span></span>

## <span data-ttu-id="98822-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98822-140">RELATED LINKS</span></span>
